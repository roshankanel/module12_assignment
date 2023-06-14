# Module 12 Report

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
   * To train and evaluate Logistic Regression models to correctly identify credtworthiness of borrowers.
* Explain what financial information the data was on, and what you needed to predict.
   * Data was related to historical data of the customer of the loan being paid. Based on this data we need to predict whether or not the loan defaults.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
   * This is giving us the count of healthy loans and non healthy loans.
* Describe the stages of the machine learning process you went through as part of this analysis.
    1. Counting rows that had score 0 (healthy) vs. score 1 (high-risk)
    2. Train-test split
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
   * The second analysis was a logistic regression model but we used the RandomOverSampler module that brought the data to 56271 from 75036
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Balanced Accuracy Score: 0.9480091532589761
    * True Negative: 18663
    * False Negative: 61
    * False Positive: 102
    * True Positive: 558
    * Accuracy [(TP+TN)/(TP+TN+FP+FN)]: 0.99
    * Healthy Loan Precision [TN/(TN+FN)]: 1.00
    * Healthy Loan Recall [TN/(TN+FP)]: 0.99
    * High-Risk Loan Precision [TP/(TP+FP)]: 0.85
    * High-Risk Loan Recall [TP/(TP+FN)]: 0.90

* Machine Learning Model 2:
    * Balanced Accuracy Score: 0.9947308560359689
    * True Negative: 55964
    * False Negative: 307
    * False Positive: 286
    * True Positive: 55985
    * Accuracy [(TP+TN)/(TP+TN+FP+FN)]: 0.99
    * Healthy Loan Precision [TN/(TN+FN)]: 1.00
    * Healthy Loan Recall [TN/(TN+FP)]: 0.99
    * High-Risk Loan Precision [TP/(TP+FP)]: 0.99
    * High-Risk Loan Recall [TP/(TP+FN)]: 0.99

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
    * The second model performed much better.   
    * Second model had a High-Risk Loan Precision of 0.99 versus the first model's 0.85 precision.
    * High-Risk Loan Recall values improved from the first model(0.90) to the second model (0.99).
    * Between the two models, the second model is recommended.
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
    * Its a known fact that high-risk loan is much worse than not granting a healthy loan. Though 
      This means that we are more concerned with False Negatives than we are with False Positives although both are important. We want to minimize False Negatives and so we want to maximize Healthy Loan Precision and High-Risk Loan     
      Recall. Healthy Loan Precision values were similar with the two models (1.00 versus 0.99). 
    
If you do not recommend any of the models, please justify your reasoning.
