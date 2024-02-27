# Challenge-12 Credit Risk Analysis Report

## Overview of the Analysis
The purpose of this credit risk analysis report is to evaluate the performance of two machine learning models in predicting credit default risk (healthy loan status as '0' vs. high-risk loan status as '1') using differenct sampling versions of the dataset. The analysis aims to ocompare the effectiveness of the models when trained on the original dataset versus a resampled version of the data.

The variable udner consideration for prediction in this analysis were related to credit default risk, which is a likely binary, indicating whether a loan status is healthy or having high-risk to default. The original dataset has 75036 loans labeled with '0'(healthy loan) and 2500 loans labeled with '1' (high-risk loan). The features as loan size, interest rate, borrower income, debt to income ratio , number of accounts, derogatory marks and total debt amount are used as factors for the model to predict results.

To conduct the credit risk analysis, the program read and preprocess original the data, and separate the data into results label data set and features data set first. In order to train the model, both the label data set and features data set are splitted into its own training and validation test sets, and model 1 chose to use the original training data while model 2 use a resampling method to balance the training data sets for the model's performance comparions and improvements. The training data sets (original or resampled) are used to fit the chosen Logistic Regression model as the machine Learning model. The fitted models with test features data input are used to predict the loan status label results, and the model performance is assessed by using appropriate metrics such as accuracy, precision, recall, F1-score, geometic mean and iba by comparing the prediction results with the given validation test labeled data to better understand the model's behavior and tune the model to generalize well to predict credit risk of loans accurately.

## Results

* Original Training Dataset Model:
  * Balanced Accuracy Score: 0.952048
  * Precision Score: '0' - 1.00, '1' - 0.85, 'average/total' - 0.99
  * Recall Score: '0' - 0.99, '1' - 0.91, 'average/total' - 0.99
  * F1 Score: '0' - 1, '1' - 0.88, 'average/total' - 0.99
  * Geometric Mean: '0' - 0.95, '1' - 0.95, 'average/total' - 0.95

* Resampled Training Dataset Model:
  * Balanced Accuracy Score: 0.993678
  * Precision Score: '0' - 1.00, '1' - 0.84, 'average/total' - 0.99
  * Recall Score: '0' - 0.99, '1' - 0.99, 'average/total' - 0.99
  * F1 Score: '0' - 1, '1' - 0.91, 'average/total' - 0.99
  * Geometric Mean: '0' - 0.99, '1' - 0.99, 'average/total' - 0.99

## Summary

The results indicate that both models perform reasonable well in predicting credit risk for the loan product, but there are some notable differences between the two training dataset (with or without resampling techniques). The resampled dataset model demonstrates higher balanced accuracy, recall, F1 scores and geometric mean compared to the original dataset model. This suggests that the resampled data, which likely balanced the classes of healthy and high-risk instances, has enabled the model to better discern patterns and make more accurate predictions, especially in identifying true positives and true negatives and reduce the false negtive predictions.

Considering the performance metrics and the goal of model is to predict the loan credit risk accurately, the resampled dataset model appears to be the better choice. The higher precision and recall scores, along with the improved balanced accuracy, indicate that the model trained on the resampled data is more reliable and effective in identifying potential credit risk of the loans. Therefore, it is recommended to utilize the resampled dataset model for credit risk predictions. It improves the model performance and provides better sights and awareness of potential credit risks existense, thus assisting in more informed decision-making processes regarding credit approvals or risk management strategies.




