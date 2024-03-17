# Credit Risk Classification Model

## Overview

The purpose of this analysis is to build a model that can identify the creditworhtines of borrowers. The model will inform the user on whether or not a loan would be healthy or has a high risk of defaulting based on certain variables that were in our data source (lending_data.csv). The variables that were provided in our data were loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, and total_debt. The data source also provided data on past loans and specified if said loans were healthy (by showing a 0) or had a high risk of defaulting (by showing a 1) in the loan_status column. We used both the variables and the loan_status column to create a model that predicted whether or not the loan would be healthy.

To start this analysis we read in the lend_data csv and put it in a dataframe. From there we created labels to hold our data. The y label held the loan_status column and the X label held the rest of our data minus the load_status column. We then split the data into training and testing datasets using the train_test_split method so that we could evaluate the performance of our model and prevent overfitting. Once we had our data split into training and testing datasets we created and fit a logistical regression model using the training data (X_train and y_train). We then used the predict method to have our model make its predictions on the X_test data. We then evaluated our model's performance by generating a confusion matrix and a classification report. 

## Results
- Accuracy Score
    - The accuracy score is a metric from the classification report that measures how accurate the model is by looking at how many correct predictions were made out of all predictions the model made. 
    - The accuracy score in our classification report was .99 representing that this model was extremely accurate in making predictions.
- Precision Score
    - The precision score is a metric from the classification report that measures how many positive predictions were actually positive. It is calculated by taking the number of true positives divided by the sum of true positives and false positives.
    - The precision scores for healthy loans (0) and high risk loans (1) were 1.00 and .87 respectively. That is incredibly high scores for both and indicates a high accuracy regarding positively made predictions.
- Recall Score
    - The recall score is a metric from the classification report that measures how many positive predictions were made out of all actual positive instances. It's calculated by taking the number of true positives divided by the sum of true positives and false negatives.
    - The recall scores for healthy loans (0) and high risk loans (1) were 1.00 and .89 respectively. Those are very high scores for both outcomes and indicates that the model is highly accuract regarding positively made predictions out of all actual positive predictions.

## Analysis Summary

Based on the classification report this logistic regression model predicted both healthy (0) and high-risk (1) loans very accurately. The model is able to perfectly predict healthy loans with precision and recall scores of 1.00. It is also fairly good at predicting high-risk loans with precision and recall scores of .87 and .89. While it is better at predicting healthy than high-risk loans, the model is still predicting high-risk loans correctly with an f1-score of 88%. The F1-score shows a balanced measure of the model's precisiona and recall scores. Overall, while we could look at further optimizing the high-risk prediction capability of the model, it is currently able to predict the creditworthiness of a borrow with a very high level of accuracy. 

