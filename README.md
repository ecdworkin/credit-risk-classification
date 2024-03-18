# credit-risk-classification
Credit Risk Classification - Module 20 Supervised Machine Learning
# MODULE 20 REPORT
## Overview of the Analysis

In this challenge, I created a machine learning model to predict whether a loan was healthy or high risk as denoted by a 0 (healthy) or 1 (high risk). The model evaluated several variables in identifying loans: loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, and total debt. Loan analysis information is critical to financial institutions as it helps them maintain an appropriate risk mix and make prudent decisions in the loan approval process.

To create the model, I used a Logistic Regression model via scikit-learn. My steps can be broken down into four parts:
    - First, I prepared the data by separating it into features (x values) and labels (y values), where features was all the variables contributing to loan status (healthy or high risk) and label was the assigned rating of healthy or high risk.
    - Second, I split the data using train_test_split. This creates two parts of the data set: one for training, and one for testing. The training set is used to train or calibrate the model, and the testing set is used to measure its accuracy.
    - Third, the model was actually trained. This step allows the model to identify the best coefficients for each feature (variable) to make predictions as acurately as possible.
    - Fourth, the model was evaluated using a confusion matrix and classification report, which allowed me to evaluate its precision (when the model says the loan is healthy, how often is it healthy?) and recall (how many of the healthy loans did it actually catch). This information can help me or the user understand where the model is successful, and where it may need improvement.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Logistic Regression Model:
    * Accuracy: The model correctly classifies 99% of all loans
    * Precision (Healthy Loans): When a loan is predicted to be healthy, the model is correct 100% of the time.
    * Precision (High-Risk Loans): When the model predicts a loan is high-risk, the model is correct 85% of the time.
    * Recall (Healthy Loans): The model correctly identifies 99% of the healthy loans.
    * Recall (High-Risk Loans): The model correctly identifies 91% of the high-risk loans.
   

## Summary

We only testes Logistic Regression for this assignment, but overall, I feel the model is useful and accurate given the binary nature of the provided CSV. A more accurate model for this example might be one that can assess the loan risk when it is put on a scale (low loans are actually graded) rather than a binary. From some research, it looks like a Gradient Boosting Machine might be more accurate as it is specifically designed to excel at evaluating risk. 

Performance and how we perceive it is dependent on the problem at hand - in the case of loans it is far more important to accurately identify high  risk loans than it is to identify healthy ones. Identifying high risk loans allows banks to better assess their overall risk exposure and blend mortgage bonds accordingly.