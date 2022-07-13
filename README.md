# Credit Card Transaction Validation: Overview

- Create a tool that has a function to evaluate and classify every credit card transaction submitted whether it is valid or fraudulent.
- A tool made using Machine Learning with a 100% accuracy rate to avoid fraud and laundering that can harm Customers and Bank.
- Using data sets published by [UCI Machine Learning Repository (Credit Approval Data Set)](https://archive.ics.uci.edu/ml/datasets/credit+approval).
- The Machine Learning model used is Logistic Regression with parameter optimization, maximum iterations and tolerance values, using Grid Search Cross Validation to produce model with the best performance.

## Code and Resources Used
**Python Version:** 3.10.3  
**Packages:** pandas, numpy, sklearn  
**Dataset source:** https://archive.ics.uci.edu/ml/datasets/credit+approval

## Data Cleaning
After collect Dataset from UCI Machine Learning Repository, I need to check and clean up the dataset to makesure no missing values on Dataset before creating a Machine Learning model. I made the following changes and created the following variables:
- Import Dataset to Data Frame with pandas.
- Change the name columns of Dataset to make it easier to understand.
- Check for missing values owned by the Dataset.
- Delete columns that are judged not to be related to the target.
- Clean up string missing values with most common values of each columns.

## Preprocessing Data
After Dataset is clean, the dataset is not quite ready to fit into the model because it is still at a different scale in each column. So, I made the following changes and created the following variables:
- Splitting dataset for test and training purpose.
- Create the dummies dataset.
- Scaling dummies dataset with values betwen minimum 0 to maximum 1.
The dataset is ready to fit into the model.

## Model Building
Because approval credit card must be fast and accurate, the machine learning classification model must be quick and strong enough. So, Logistic regression with parameter optimization can be suitable for use.
- Creat multiple case of parameters for Logistic regression.
- Fitting dummies dataset training to model via Grid Search Crossvalidation.
- Estimator score evaluation and save the model with best estimator.
- Predict dummies dataset test and show the result on Confusion Matrix

## Model performance
**Best parameter:**
- Maximum Iteration = 100
- Tolerance value = 0.01  

**Best Score:**
- Estimator score = 1.0000 (Prediction 100% accurate)
