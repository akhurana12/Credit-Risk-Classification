# Credit-Risk-Classification
 
# Overview of the Analysis

The purpose of this analysis was to build a machine learning model and evaluate it to determine whether it would be able to appropriately predict how worthy a potential borrower would be of a loan based on their credit. The historical data obtained from a peer-to-peer      lending services company that the model was being based on included information on a number of factors that overall were indicative of their credit such as the following: the size of the loan, interest rate, income of the borrower, debt to income ration, the number of accounts and derogatory remarks they had and the total debt with the resulting loan status. The model was designed to take into account the various factors and predict the creditworthiness of borrowers.

The machine learning model developed was intended to help make a prediction on which loans are either low-risk and hence considered healthy or high-risk using the logistic regression method. However, the results of the evaluation of the model developed using the logistic regression method had varying recall rates despite having an accuracy of approximately 95%, which indicated that the dataset being used was imbalanced with most of the data having health loans as opposed to non-healthy. Taking this further, the data was resampled using the oversampling method to develop the model with a more balanced data set which resulted in an accuracy  and recall rate of approximately 99%, indicating that it was a more robust prediction tool.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Balanced Accuracy: 95% 
  * Overall Precision: 99%
  * Overall Recall Score: 99%

              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384

* Machine Learning Model 2: Oversampling method
   * Balanced Accuracy: >99% 
   * Precision: 99%
   * Recall Score: 99%

               precision    recall  f1-score   support

           0       0.99      0.99      0.99     75036
           1       0.99      0.99      0.99     75036

    accuracy                           0.99    150072
   macro avg       0.99      0.99      0.99    150072
weighted avg       0.99      0.99      0.99    150072

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

I would recommend using machine learning model 2 as based on the evaluation values, it is more robust in terms of accuracy as the model based on the original data set was not as accurate as it only predicted high-risk loans accurately 85% of the time which would not be appropriate to use in the situation. The imbalance in the data was also demonstrated when using the value_counts function for model 1 as seen below:

0    75036
1     2500
Name: loan_status, dtype: int64

In model 2 the data was balanced with the same number of distinct values for both scenarios to build the model based on as indicated below:

{0: 75036, 1: 75036}