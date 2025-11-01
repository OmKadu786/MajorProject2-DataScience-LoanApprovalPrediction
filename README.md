# MajorProject2-DataScience-LoanApprovalPrediction

📘 Overview

This project applies machine learning classification algorithms to predict whether a person’s loan application will be approved based on socio-economic and credit-related attributes.
The model leverages Python (scikit-learn) for data preprocessing, visualization, model training, and evaluation.

🎯 Objective

To build a classification model that can:
Accurately predict loan approval status (“Approved” / “Rejected”), and
Help financial institutions automate and improve decision-making by identifying high-probability applicants.

🧩 Dataset
File: loan_approval_dataset.csv
Source: Open / Kaggle dataset
Target Variable: loan_status (Approved → 1, Rejected → 0)

  Key Features
  | Feature             | Description                  |
  | ------------------- | ---------------------------- |
  | `Gender`            | Applicant’s gender           |
  | `Married`           | Marital status               |
  | `Dependents`        | Number of dependents         |
  | `Education`         | Graduate or Not Graduate     |
  | `Self_Employed`     | Employment status            |
  | `ApplicantIncome`   | Income of applicant          |
  | `CoapplicantIncome` | Income of co-applicant       |
  | `LoanAmount`        | Loan amount in thousands     |
  | `Loan_Amount_Term`  | Term of loan in months       |
  | `Credit_History`    | 1 = Good history, 0 = Bad    |
  | `Property_Area`     | Urban / Semiurban / Rural    |
  | `Loan_Status`       | Target — Approved / Rejected |

⚙️ Workflow

1. Data Loading
Load dataset using pandas.
Check column names, data types, and null values.
Strip unwanted spaces in column names and values.

2. Data Cleaning & Preprocessing
Convert text to lowercase for consistency.
Handle missing values using median/mode imputation.
Encode categorical variables using LabelEncoder.
Encode target: approved → 1, rejected → 0.
Apply StandardScaler to normalize numerical features.

3. Exploratory Data Analysis (EDA)
Compare loan approval rates for:
Graduates vs Non-Graduates
Self-employed vs Not self-employed
Visualize correlation matrix using Seaborn heatmap.
Generate boxplots to detect outliers in numeric features.

🧠 Sample Findings

Graduates tend to have a slightly higher loan approval rate.
Applicants with good credit history or higher income have better approval odds.
Self-employed applicants show slightly lower approval percentages on average.

🧮 Model Building
  Algorithms Used
  | Model                            | Type                       | Library      |
  | -------------------------------- | -------------------------- | ------------ |
  | **Logistic Regression**          | Linear classifier          | scikit-learn |
  | **Decision Tree Classifier**     | Non-linear model           | scikit-learn |
  | **Random Forest Classifier**     | Ensemble of decision trees | scikit-learn |
  | **Support Vector Machine (SVM)** | Kernel-based classifier    | scikit-learn |

  Data Split

  Training Set: 80%
  Testing Set: 20%
  Evaluation Metrics
  Accuracy
  Precision
  Recall
  F1-Score
  ROC-AUC Score
