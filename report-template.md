# Module 12 Report Template

## Overview of the Analysis

I used a machine learning model to determine if loans are safe (low-risk) or risky (high-risk) based on the loan status provided by the lending company.

After analyzing the lending company's dataset, I developed a Logistic Regression Model that achieved an accuracy score of 99%. However, when it comes to distinguishing non-healthy loans, the model's recall value is lower (0.91) compared to its recall value for healthy loans (0.99). This suggests that the model performs better at predicting loan status as healthy rather than identifying loan status as non-healthy. The reason behind this discrepancy lies in the dataset's imbalance, where the majority of the data corresponds to one class label (in this case, healthy loans greatly outnumber non-healthy loans).

To mitigate this issue, resampling the data was completed using a random over sampler that added values to the minority class and stabilized the values of the majority class to balance the tables.

## Results

Machine Learning Model 1 with original data:

* 56 false positives (actual value: healthy, predicted value: non-healthy)
* 102 false negatives (actual value: non-healthy, predicted value: healthy)
* Balanced accuracy of 95.2% overall accuracy of 99%

Machine Learning Model 2 with resampled data:

* 422 false positives (actual value: healthy, predicted value: non-healthy)
* 403 false negatives (actual value: non-healthy, predicted value: healthy)
* Balanced accuracy of 99.5% and an overall accuracy of 99%

## Summary

A lending company wants a model that accurately distinguishes between healthy and non-healthy loans to minimize potential costs. Misclassifying healthy loans as non-healthy can lead to customer loss, while misclassifying non-healthy loans as healthy can result in financial losses for the company.

The Logistic Regression model trained with resampled data performed better than the model trained the original data. The balanced dataset approach improved accuracy and recall, reducing errors in classifying non-healthy loans.

The resampled data provides a more accurate look as the data is determined to be 99.5% accurate coming into the analysis. The original data lagged behind with an accuracy of 95.2% coming into the analysis. While the overall accuracies were the same, I feel more comfortable using more data to add complexity and strength to the model and ensuring a more accurate overall result to the client.

