# CKD AAAI 2024

Lawrence Huang BS, Keyvon Rashidi BSE, Sachin Shankar MS, Dany Alkurdi AB, Felipe Giuste PhD

Stages of data processing
1. read in MIMIC-IV dataset with SQL script and join on relevant tables in relational format
  - included tables such as demographics, diagnoses
1. determine CKD status from ICD codes
1. examine most prevalent non-CKD codes associated with CKD patients to determine feature set (prevalence-based feature selection)
1. preprocess data into one-hot encoded ICD codes, split data into train / test sets
1. train 3 different machine learning models on training data to predict CKD status (Logistic Regression, kNN, Random Forest)
1. evaluate model performance on test set with AUROC, select model threshold with best tradeoff of sensitivity / specificity and evaluate confusion matrix of that model
1. best model was RandomForest
