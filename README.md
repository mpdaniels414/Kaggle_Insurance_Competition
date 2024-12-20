# 2024 Kaggle Playground Series: Predicting Insurance Premiums

## Overview

This project is part of the **2024 Kaggle Playground Series**, designed to help participants practice and improve their machine learning skills using synthetic datasets. The goal of this competition is to predict **insurance premiums** based on various factors using a dataset provided by Kaggle.

### Evaluation Metric

Submissions are evaluated using the **Root Mean Squared Logarithmic Error (RMSLE)**. This metric emphasizes accuracy and penalizes large deviations in log-transformed predictions.

---

## How to Access the Data

To download the dataset and participate in the competition:

1. Visit the competition page: [Kaggle Playground Series S4E12](https://www.kaggle.com/competitions/playground-series-s4e12/overview).
2. Sign in or create a Kaggle account.
3. Accept the competition rules.
4. Download the dataset from the **Data** tab.

---

## Code Explanation

### **Kaggle_Insurance.ipynb**

This notebook implements the full machine learning pipeline to predict insurance premiums. Below are the key steps:

#### **1. Data Preprocessing**
- Handles missing values by imputing or removing them.
- Encodes categorical features using `LabelEncoder`.
- Scales numeric features with `StandardScaler` for normalization.

#### **2. Exploratory Data Analysis (EDA)**
- Analyzes the distribution of key features.
- Identifies correlations between predictors and the target variable (`Premium Amount`).
- Guides feature engineering by examining trends in feature importance.

#### **3. Model Training**
- Implements **XGBoost Regressor**, a gradient boosting framework, for robust predictions.
- Splits data into training and testing sets (80-20 split).
- Tunes hyperparameters using `RandomizedSearchCV`.

#### **4. Model Evaluation**
- Evaluates the model with:
  - **Root Mean Squared Logarithmic Error (RMSLE)** – competition evaluation metric.
  - **R² Score** – measures model fit.
  - **Mean Squared Error (MSE)** – secondary performance metric.

#### **5. Prediction and Submission**
- Generates predictions for the test dataset.
- Prepares the submission file in the required format:


---

### **Kaggle_Insurance_EDA.ipynb**

This notebook focuses on **Exploratory Data Analysis (EDA)** to gain insights into the dataset. Key steps include:

#### **1. Feature Analysis**
- Examines distributions of numerical and categorical features.
- Identifies missing values and inconsistencies.

#### **2. Visualizations**
- Uses histograms, box plots, and scatter plots to explore feature relationships with the target (`Premium Amount`).
- Generates a heatmap to highlight feature correlations.

#### **3. Insights Extraction**
- Identifies key drivers of insurance premiums, such as demographic and policy-related features.
- Recommends feature engineering strategies based on trends.

#### **4. Target Variable Analysis**
- Analyzes the distribution of `Premium Amount` to detect skewness or other characteristics that might influence model performance.

---
