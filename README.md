# BinaryClassification_EDA_with_Python
A detailed notebook to deal with Binary Classification Problem without having any clue of input columns

## Task
Binary Classification - Do an exploratory analysis of the dataset provided, decide on feature selection, preprocessing before training a model to classify as class ‘0’ or class ‘1’.

## Given files 
1.	training_set.csv - To be used as training and validation set - 3910 records, 57 features, 1 output
2.	test_set.csv (without Ground Truth) - 691 records, 57 features

## Quick Description
1.	Readme file - explaining any relevant thought process as well as the general approach for the task
    Any approch to solve a classification problem is to target acceptable F1 Score, or Precision | Recall according to the business problem.
    In our case, The business problem is invisble as data does not contain neither any categorical values nor any column descriptions. This leads us to solely depend       on our capabilities to understand the data and identify the features.
    Understanding the data: 
    Data contain 57 independent columns for 1 dependent variable (output column). To understand the impact and pattern of all the columns in bulk (as taking one by one        is not a feasible option). I calculated all the columns :
    -Data Types
    -Description (min, max, std)
    -Null/Missing Values
    -Output column distribution (to understand data is imbalance or balanced)
    -Correlation
    -Multicollinearity using VIF
    -Feature Importance using Logistic Regression and Random Forest Classifier
    -Dimenssionality Reduction (PCA)
2.	Model performance analysis on validation set in terms of various risks
    - Started with Niave Bayes on raw data to understand the scope of improvement 
    - SVM, then Logistic Regression and then Random Forest Classifier, and then ANN (not required for this data as we are getting accuracies over 90% without                 introducing heavy models)

3.	A list of dependencies/libraries & their versions to run the code.
    Python and its libraries as stated in notebook
  
4. Result:
    RandomForest Classifier was able to give accuracy ~94% and with a balanced confusion matrix without doing any Dimenssionality Reduction

