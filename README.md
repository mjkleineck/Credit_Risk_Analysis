# Credit Risk Analysis

## Overview
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. We’ll need to employ different techniques to train and evaluate models with unbalanced classes. The purpose of this analysis is to test and identify the best machine learning algorithms to predict low-risk and high risk loans.

## Results

### Naive Random Oversampling

![Naive Random Oversampling](https://github.com/mjkleineck/Credit_Risk_Analysis/blob/main/Resources/Naive-Random-Oversampling.png)

* Balanced Accuracy Score: 0.6596
* Precision Score:
    - High Risk: 0.01
    - Low Risk: 1.00
* Recall Score:
    - High Risk: 0.72
    - Low Risk: 0.60

### SMOTE Oversampling

![SMOTE Oversampling](https://github.com/mjkleineck/Credit_Risk_Analysis/blob/main/Resources/SMOTE-Oversampling.png)

* Balanced Accuracy Score: 0.6628
* Precision Score:
    - High Risk: 0.01
    - Low Risk: 1.00
* Recall Score:
    - High Risk: 0.63
    - Low Risk: 0.69

### Undersampling (Cluster Centroids)

![Undersampling (Cluster Centroids)](https://github.com/mjkleineck/Credit_Risk_Analysis/blob/main/Resources/Undersampling-Cluster-Centroids.png)

* Balanced Accuracy Score: 0.5447
* Precision Score:
    - High Risk: 0.01
    - Low Risk: 1.00
* Recall Score:
    - High Risk: 0.69
    - Low Risk: 0.40

### Combination (Over and Under) Sampling - SMOTEENN

![Combination (Over and Under) Sampling - SMOTEENN](https://github.com/mjkleineck/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN.png)

* Balanced Accuracy Score: 0.6445
* Precision Score:
    - High Risk: 0.01
    - Low Risk: 1.00
* Recall Score:
    - High Risk: 0.72
    - Low Risk: 0.57

### Balanced Random Forest Classifier

![Balanced Random Forest Classifier](https://github.com/mjkleineck/Credit_Risk_Analysis/blob/main/Resources/Balanced-Random-Forest-Classifier.png)

* Balanced Accuracy Score: 0.7885
* Precision Score:
    - High Risk: 0.03
    - Low Risk: 1.00
* Recall Score:
    - High Risk: 0.70
    - Low Risk: 0.87

### Easy Ensemble AdaBoost Classifier

![Easy Ensemble AdaBoost Classifier](https://github.com/mjkleineck/Credit_Risk_Analysis/blob/main/Resources/AdaBoost-Classifier.png)

* Balanced Accuracy Score: 0.9317
* Precision Score:
    - High Risk: 0.09
    - Low Risk: 1.00
* Recall Score:
    - High Risk: 0.92
    - Low Risk: 0.94

## Summary

With identifying low-risk and high-risk loans, all of the models did a good job at identifying low-risk loans. This make sense because the data set was skewed towards low-risk loans to begin with. Due to the nature of the loan business, we want to be sensitive towards identifying the high-risk loans so we can catch them before they are approved and vet the borrower further to ensure they are fit to lend to. Our success metric is the Recall Score of High-Risk loans. The Easy Ensemble AdaBoost Classifier performed the best in relation to the Recall Score of High-Risk loans. Thus, we recommend using this predictive model to identify High Risk loans in the future.