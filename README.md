# Credit Risk Classification

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* In this Challenge, we used various supervised machine leanring techniques to train and evaluate a model based on loan risk. By using a dataset of historical lending activity from a peer-to-peer lending services company we built a model that can identify the creditworthiness of borrowers (high/low risk borrowers).
* The dataset included loan size, interest rate, borrower income, debt-to-income ratio, number of accounts borrowers had, number of derogatory marks, and total debt. With this financial information, we predicted if the loan is low or high risk (0 equates to a healthy loan and 1 equates to high risk of defaulting).
* With this information, we restructured the dataframe by loan status (0 and 1) and used value_counts to predict with original data (0: 75036 an 1: 2500) and resampled data (0: 56271 and 1: 56271).
* In the original and resampled logistic regression model, the following were stages of the process:
    * Fit the model using training data by instantiating the model and assigning a random_state parameter of 1 to the model.
    * Calculate accuracy score of the model.
In resampled logistic regression model, there was an additional step of using the RandomOverSampler module to resample the data, to ensure equal number of data points.

## Results

* Machine Learning Model 1:
  * Logistic Regression with Original Data: 
    - Accuracy: 95% 
    - Precision:
        - Healthy loan (0): 100%
        - High-risk loan (1): 85%
    - Recall: 99%
* Machine Learning Model 2:
  * Logistic Regression with Resampled Data: 
    - Accuracy: 99%
    - Precision:
        - Healthy loan (0): 100%
        - High-risk loan (1): 84%
    - Recall: 99% 


## Summary

Based on the results above, the logistic regression model with resampled data peformed best and most accurately. The precision score for predicting healthy loans (0) is the same for Model 1 and Model 2, however, there is a higher accuracy with the resampled data in Model 2 at 99%. It is important to predict the high risk loans (1) to ensure minimal risks and reduce the number of defaulters.
