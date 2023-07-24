# credit-risk-classification
Module 20 Challenge

## Background
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the credit worthiness of borrowers.

## Data Source
[lending_data.csv](Credit_Risk/Resources/lending_data.csv)

## Instructions
The instructions for this Challenge are divided into the following subsections:

### 1. Split the Data into Training and Testing Sets
View of original DataFrame
![](Credit_Risk/Images/Original%20data.png)

### 2. Create a Logistic Regression Model with the Original Data
 Classification report using Original Data
![](Credit_Risk/Images/Classification%20report.png)

The logistic regression model predicts a healthy loan extremely well with a 100% precision and recall. The 100% recall indicates that is able to identify all of the healthy loan candidates. It's ability to predict a high-risk loan is good, but not with the same high precision as the healthy loan. The precision on the high-risk loan prediction is 87% with 89% recall.

### 3. Create a Logistic Regression Model with the Resampled Training Data
Classification report using Resampled Training Data (RandomOverSampler)
![](Credit_Risk/Images/Oversampled%20classification%20report.png)

The oversampled data certainly improves the accuracy of the model. It greatly increased the precision and recall for the high-risk loans, which is a valuable improvement from 87% precision to 99% precision. The precision of the healthy loan was lowered very slightly from 100% to 99%, however, the oversampled model has better accuracy overall and will help to eliminate the mistake of high-risk loans.

Random oversampling involves randomly duplicating examples from the minority class and adding them to the training dataset. Oversampling improves the model training and increases accuracy.

### 4. Credit Risk Analysis Report

* The purpose is to build a model that can identify the credit worthiness of borrowers and then evaluate the findings of the trained data model results to determine if we recommend the model for use.
* The provided financial data is a dataset of historical lending activity from a peer-to-peer lending services company. The machine learning model was used to predict whether or not a new loan applicant is credit-worthy and considered as a healthy loan or high-risk loan candidate.
* The linear regression machine learning model was built to predict the loan_status (Healthy Loan (0) or High-risk Loan (1)). The loan_status column is our y. The X values are loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, and total_debt. 
* Brief overview of the stages of the machine learning process for this analysis:
    * Separate y label from the X features.
    * Check the quantity of labels in the dataset using value counts on y.
    * Split the data into training and testing datasets by using train_test_split.
    * Create a Logistic Regression Model with the Original Data. Evaluate this model’s performance with a balanced accuracy score, confusion matrix, and classification report.
    * Create a Logistic Regression Model with the Resampled TrainingData. Evaluate this model’s performance with a balanced accuracy score, confusion matrix, and classification report.


## Results

Machine Learning Model with Original Data:
  * Accuracy: 0.944
  * Precision Predicting Healthy Loan: 1.00
  * Recall Healthy Loan: 1.00
  * Precision Predicting High-risk Loan: 0.87
  * Recall High-risk Loan: 0.89


Machine Learning Model with the Resampled Training Data:
  * Accuracy: 0.994
  * Precision Predicting Healthy Loan: 0.99
  * Recall Healthy Loan: 0.99
  * Precision Predicting High-risk Loan: 0.99
  * Recall High-risk Loan: 0.99


## Summary

The Linear Regression machine learning model with the original data predicts a healthy loan extremely well with a 100% precision and recall. The 100% recall indicates that is able to identify all of the healthy loan candidates. It's ability to predict a high-risk loan is good, but not with the same high precision as the healthy loan. This is a less effective model as it will not identify all high-risk loans, allowing for some false negatives (approval of loans thought to be healthy that are actually high-risk).

The Linear Regression machine learning model with the oversampled data certainly improves the accuracy of the model by increasing the precision and recall for the high-risk loans. This is a valuable improvement from 87% precision to 99% precision. The precision of the healthy loan was lowered very slightly from 100% to 99%, however, the oversampled model has better accuracy overall and will help to eliminate the mistake of high-risk loans.

I recommend the oversampler model for use by the credit company as it will allow them to effectively identify both healthy loan and high-risk loan applicants at a high rate. Being able to identify the high-risk loans is critical to avoiding the approval of non-credit-worthy loans, which are costly to a credit company.   

