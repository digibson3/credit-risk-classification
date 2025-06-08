# Module 12 Report Template

## Overview of the Analysis

This analysis aimed to predict credit risk by classifying loans as either 0 (healthy loan) or 1 (high-risk loan) using supervised machine learning. The dataset contained financial information on individual loans, including factors like interest rate, income, and debt-to-income ratio.

The goal was to determine whether a given loan should be considered high-risk or healthy, enabling better risk management and lending decisions.

Data Overview
Target Variable: loan_status

0: Healthy Loan

1: High-Risk Loan

Features: All other columns excluding loan_status, including financial metrics such as interest rate, loan size, and income.

python
Copy
Edit

# Sample class distribution
y.value_counts()
This code confirms the dataset is imbalanced, with far more healthy loans than high-risk ones.

Machine Learning Process
Data Splitting:

Data was divided into training and testing sets using train_test_split, with a 75/25 split and stratification to preserve class balance.

Model Selection:

A Logistic Regression model was trained using LogisticRegression(solver='lbfgs', random_state=1).

Model Evaluation:

Predictions were evaluated using a confusion matrix and classification report.

Key metrics considered: accuracy, precision, recall.

Results
Machine Learning Model 1: Logistic Regression

Accuracy: High overall accuracy.

Healthy Loans (0)

Correct predictions: 18,673 out of 18,759

Precision and recall were both very high.

High-Risk Loans (1)

Correct predictions: 593 out of 625

Model missed 32 high-risk loans (false negatives)

Summary
The logistic regression model showed strong performance, particularly in identifying healthy loans. It was also fairly accurate at detecting high-risk loans, but did miss a small number, which could be critical in financial decision-making.


