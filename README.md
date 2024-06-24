## Overview of the Analysis

In this Challenge, various techniques will be utilized to train and evaluate a model centered on loan risk. A dataset of historical lending activity from a peer- to peer lending services company will be employed to construct a model capable of identifying the credit worthiness of borrowers. Challenge breakdown:

* A analysis of the models and whether they can accurately predict an outcome of healthy or high risk.
* Financial data includes loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, total debt and loan status(target).
* The model will use predict a 0 (healthy) or 1 (high-risk) as a loan status.
* Describe the stages of the machine learning process you went through as part of this analysis.
* Stages of the modeling: Loading dataset, separating of target and features, splitting data using train_test_split, fitting logistic regression model to the training data, saving prediction in order to evaluate and creating a confusion matrix and classification report.
* Methods used: logistic Regression.

## Instructions

The instructions for this Challenge are divided into the following subsections:
* Split the Data into Training and Testing Sets
* Create a Logistic Regression Model with the Original Data
* Write a Credit Risk Analysis Report

## Split the Data into Training and Testing Sets

1. Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
2. Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
3. Split the data into training and testing datasets by using train_test_split.

## Create a Logistic Regression Model with the Original Data

Use knowledge of logistic regression to complete the following steps:
1. Fit a logistic regression model by using the training data (X_train and y_train).
2. Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
3. Evaluate the model’s performance by doing the following:
   - Generate a confusion matrix.
   - Print the classification report.
4. Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?


## Results

Scores.

* Machine Learning Model:
    * Model accuracy over all 99%.
    * Precision for 0(healthy) 100%. Precision for 1(high-risk) 87%.
    * Recall for 0(healthy) 100%. Precision for 1(high-risk) 89%.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* The model was able to accurately predict a 1(healthy) and preformed much better than predicting a 1(high-risk).
* Even though the model worked better on healthy loans it did not have enough instances of a high-risk loan to be able to fully train. healthy had 18,759 instances where high-risk only had 625. Training dataset needs more data for a loan status on 1.
* the problem needed to be solved is accurately predicting 1(high-risk) loans rather than healthy. Getting a false negative, or miss predicting high-risk loan as a healthy loan, can cost the client financially and potentially render this model as ineffective.

As the model is now, it does perform well in a basic sense. It's accuracy is 99% and individually 0 and 1 accuracy is over 70%. However, for the purpose for creating a loan risk model I do not think 87% accuracy on high-risk is good enough for the client. If more high risk data is provided, or if high-risk was given more weight it would be better to test on this model before considering making a new model. 

