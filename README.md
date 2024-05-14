# credit-risk-classification

# Module 20 Challenge

## Overview of the Analysis

* The purpose of the analysis was to develope a machine learnging model to predict the risk of the loans `0` (healthy loans), `1` (high-risk loans). This would help finacncial institutions and credit agencies dteremine who they should lend to based on the model we created. 
* The financial information consisted of these variables: `loan_size`, `interest_rate`, `borrower_income`, `debt_to_income`, `num_of_accounts`, `derogatory_marks`, `total_debt`, `loan_status`. The goal was to use the data to predict whether a loan is healthy or not: if `loan_status` is `1` it's a high-risk loan, if `loan_status` is `0` it's a healthy loan.
* The goal was to prdict `loan_status` based on the `LogisticRegression` model.
* Steps in the machine learning process
    - First we needed to prepare the data from `lending_data.csv` where we put it into a data frame and set the `y` variable to the the `loan_status` column and the `X` to the rest of the columns. The goal was to predict why base on the `X` variables.
    - We then utilized the `train_test_split()` function to get the `X_train`, `X_test`, `y_train`, and `y_test` variables.
    - We then used the `LogisticRegression` model to and trained that model on our `X_train` and `y_train` data.
    - We used then created `predictions` with the `X_test` to create a confusion matrix.
    - The confusion matrix was used to ensure the `classification_report` was accurate.

## Results

* Machine Learning Model 1: Logistic Regression
    - Accuracy: The logistic regression model has an overall accuracy of 99%, indicating that it correctly predicts the loan status (healthy or high-risk) 99% of the time.
    - Precision: We can see that all instances of healthy loans had 100% precision. While high-risk loans only had an 85% precision, this could be because there are more healthy loans than high-risk loans or that our model is too simple.  
    - Recall scores: 99% of healthy loans are correctly labeled by the model, meaning very few false negatives. While 91% of high-risk loans are correctly labeled by the model, meaning 9% of the high-risk loans are not correctly labeled. 


## Summary

The logistic regression model performs best overall, achieving high accuracy and strong precision and recall scores, particularly for healthy loans. This indicates that the model is reliable in predicting loan status.

If we were to use another model I would recommend using Gradient Boosting or Random Forests because both of these learning models can handle class imbalances which this data set has an issue with. It's bed to be better at predicting whether a loan is high-risk or not because a business does not want to lose money. Healthy loans are no brainer's as it's guaranteed to give a return on investment. 