# CREDIT RISK ANALYSIS

To predict credit risk, evaluate the performance of different Machine Learning models.
Dataset was split into inputs and outputs. Since the data is imbalanced we will incorporate sampling strategies to improve the model's prediction for Credit Loss or risk.

## Purpose

- To train and evaluate models with various criteria (inputs) to determine the best model that accurately predicts credit risk.

## Resource

- Jupyter Lab v2.2.6
- VS Code v1.52.1
- Data Resource - LoanStats_2019Q1.csv

## Process / Steps

- Clean data, fit anf train data
- Methodologies -
    - Naive Random Over Sampling
    - SMOTE Over Samoling
    - Cluster Centroids Under Sampling
    - SMOTEENN a combined sampling 
    - Balanced Random Forest Classifier
    - AdaBoost (Adaptive Boost) Classifier
- Using Logistic Regression for prediction
- Accuracy of the model
- Confusion Matrix
- Imbalance Classification Report.

## Results

### (1) **Naive Random Sampling**

![ros](resources/ros.png)

### (2) **SMOTE Over Sampling**

![SMOTE](resources/smote.png)

### (3) **Cluster Centroids Under-Sampling**

![CC](resources/cc.png)

### (4) **SMOTEENN**

![SMOTEENN](resources/smottenn.png)

### (5) **Balanced Random Forest Classifier**

![Forest_Classifier](resources/rfc.png)

### (6) **Adaptive boost (Easy Ensemble Classifier)**

![AdaBoost](resources/eec.png)

- Balanced Accuracy Scores:
A. Naive Random Sampling - 65.0
B. SMOTE Over Sampling -  66.21
C. Cluster Centroids Under Sampling - 54.7
D. SMOTEENN a combined sampling - 67.7
E. Balanced Random Forest Classifier - 78.8
F. Easy Ensemble Adaptive Boost Classifier - 93.1

Observation noted during accuracy scores for each model ranges from 65% up to 93%. This accuracy score is due to the dataset and its imbalance or sensitivity to class sizes. None the less the model Easy Ensemble AdaBoost Classifier which stands out from all the other models trial.

- Precision Scores:
A. Naive Random Sampling - 0.01
B. SMOTE Over Sampling -  0.01
C. Cluster Centroids Under Sampling - 0.00
D. SMOTEENN a combined sampling - 0.01
E. Balanced Random Forest Classifier - 0.03
F. Easy Ensemble Adaptive Boost Classifier - 0.09

- Sensitivity Scores:
A. Naive Random Sampling - 0.69
B. SMOTE Over Sampling -  0.63
C. Cluster Centroids Under Sampling - 0.68
D. SMOTEENN a combined sampling - 0.78
E. Balanced Random Forest Classifier - 0.90
F. Easy Ensemble Adaptive Boost Classifier - 0.92  

## Summary

- Analysis of various model predictions show us and narrate to us that all models have a very low precision score for predicting high risk applications.
- Since the imbalance with the data set there is a majority of Low risk applications hence predictions scores on low risk applications are noticed to be more or (more confident) with its prediction.
- I would consider the most important takeaway here is the false positives. or a Type 2 error, potential high risk candidates were classified or predicted to be low risk.which means in every scenario predicted there has been a constant number of applications classified as Low-Risk avg 34-35 candidates.
- The Easy Ensemble Adaptive model is a good model to consider for use considering an accuracy score of 93.1, with sensitivity (recall) score at 0.92 which had a good prediction run of identifying a substantial number of low risk candidates.