%%writefile README.md

# CrediWise — Loan Approval Prediction System

## Overview

CrediWise is a Machine Learning-based Loan Approval Prediction System that predicts whether a loan application is likely to be approved based on applicant financial, demographic, employment, and credit-related information.

The project follows a complete Machine Learning workflow including data cleaning, exploratory data analysis, feature encoding, feature scaling, feature engineering, model training, and model evaluation.

## Dataset

The project uses `loan_approval_data.csv`.

Important features include:

- Applicant Income
- Credit Score
- Savings
- DTI Ratio
- Education Level
- Employment Status
- Marital Status
- Loan Purpose
- Property Area
- Gender
- Employer Category

Target variable:

- `Loan_Approved`

## Project Workflow

Raw Dataset
→ Data Cleaning
→ Missing Value Handling
→ EDA
→ Feature Encoding
→ Correlation Analysis
→ Train-Test Split
→ Feature Scaling
→ Model Training
→ Feature Engineering
→ Model Evaluation
→ Model Comparison

## Data Preprocessing

### Missing Values

Numerical missing values are handled using mean imputation.

Categorical missing values are handled using the most frequent value.

### Feature Encoding

Label Encoding is applied to:

- `Education_Level`
- `Loan_Approved`

One-Hot Encoding is applied to:

- `Employment_Status`
- `Marital_Status`
- `Loan_Purpose`
- `Property_Area`
- `Gender`
- `Employer_Category`

### Feature Scaling

`StandardScaler` is used to standardize the feature values before model training.

## Exploratory Data Analysis

The project performs:

- Loan approval distribution analysis
- Gender distribution analysis
- Applicant income distribution
- Outlier detection
- Credit score analysis
- Correlation analysis
- Correlation heatmap

## Machine Learning Models

Three classification algorithms are compared:

### 1. Logistic Regression

Used as a linear classification baseline.

### 2. K-Nearest Neighbors

KNN predicts the class based on the nearest observations.

`n_neighbors = 3`

### 3. Gaussian Naive Bayes

Gaussian Naive Bayes is a probability-based classification algorithm suitable for continuous features.

## Feature Engineering

Additional squared features are created:

- `credit_score_sq`
- `DTI_ratio_sq`

These features are intended to help models capture nonlinear relationships.

## Evaluation Metrics

The models are evaluated using:

- Accuracy
- Precision
- Recall
- Confusion Matrix

## Model Comparison

The performance of Logistic Regression, KNN, and Gaussian Naive Bayes is compared using the same test dataset.

Based on the current experiment, Gaussian Naive Bayes produced the best overall results among the evaluated models.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Machine Learning Concepts

This project demonstrates:

- Data preprocessing
- Missing value imputation
- Exploratory Data Analysis
- Label Encoding
- One-Hot Encoding
- Feature Scaling
- Correlation Analysis
- Feature Engineering
- Train-Test Split
- Logistic Regression
- KNN
- Naive Bayes
- Classification Metrics
- Confusion Matrix
- Model Comparison

## Future Improvements

- Cross-validation
- Hyperparameter tuning
- GridSearchCV
- ROC-AUC evaluation
- Precision-Recall curves
- Handling class imbalance
- Pipeline and ColumnTransformer
- Model deployment using Flask or FastAPI
- Web-based loan prediction interface

## Author

Shiva Kumar