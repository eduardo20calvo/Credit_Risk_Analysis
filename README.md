# Module 12 Report Template

## Overview of the Analysis

Credit risk poses a classification problem that's inherently imbalanced. This is beacuse haelthy loans easily outnumber risky loans. 
The purpose of this analysis is to help a peer-to-peer lending services company build a model that can identify the creditworthiness
of borrowers. The dataset used was from a csv file showing the historial lending activity from the company. The variable that we 
were trying to predict was the loan status using a list of feature or characteristics of different loans including loan size and
interest rate. We imported our dependencies and libraries and loaded the csv file into a DataFrame. We set the features from the
dataset into the X variable and the loan status of each loan as the y variable. Then we check the balance of the variables and 
split the data into traininfg and testing datasets. We use the Logistic Regression Model to predict the loan statuses using 
the original data and by oversampling the data. Finally, we evaluated each model's performance by calculating the accuracy score
of the model and by creating a confusion matrix and classification report, by using 0["healthy loan"] and 1["high-risk loan"] 
as the results.

## Results

For the first Logistic Regression Model using the original dataset, we obtained the following metrics:

  * Balanced Accuracy Score:
    * 95%

  * Precision:
    * 100% for the healthy loan
    * 85% for the high-risk loan

  * Recall:
    * 99% for the healthy loan
    * 91% for the high-risk loan

For the last Logistic Regression Model using the oversampled dataset, we obtained the following metrics:

  * Balanced Accuracy Score:
    * 99%

  * Precision:
    * 100% for the healthy loan
    * 84% for the high-risk loan

  * Recall:
    * 99% for the healthy loan
    * 99% for the high-risk loan

## Summary

Our findings indicate that the Logistic Regression Model that uses the oversampled data performed much better than the model using 
the original data. This can be seen as the model fitted with the oversampled data had a higher balanced accuracy score by 4% and a higher 
recall for the high-risk loans by 8%. Although the model fitted with the oversampled data had a slightly lower precision than the previous
model on the high-risk loan by 1%, this is offset by the higher recall. The performance on these models depends on the prediction on the 
high-risk loans as the metrics for the healthy loans are about the same. For this particular dataset, it is recommended to use the 
Logistic Regression Model fitted with the oversampled data as the accuracy and recall is higher than the model fitted with the original
data.

