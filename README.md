# Overview

Purpose of this project is to apply different machine sampling technquies and models to loans stastical data which has unbalanced classes of risks & identify which works best with the data. I used various sampling techniques to identify which technique works best with the data. Oversampling like RandomOverSampling & SMOTEE, undersampling like ClusterCentroid & combination of both that is SMOTEEN is applied. Also, 2 other algorithms like BalancedRandomForestClassifier and EasyEnsembleClassifier are applied on the data set to see if they provide more desired result.

# Results

Here are the results of the six machine learning models/techniques we applied on the loans data and how they are compared against each other in precision, recall, balanced accuracy & f1 score:

## 1. Naive Random Oversampling

![balance accuracy](https://github.com/hemalis/credit_risk_analysis/blob/main/images/RandomSampling.png?raw=true)

_Balanced accuracy score:_ 0.6511924140262483

_Precision_ is **0.01** for high-risk loans and **1.00** for low-risk loans

_Recall_ is **0.74** for high-risk loans and **0.56** for low-risk loans

_Average Precision_ is **0.99** and _Average Recall_ is **0.56**

## 2. SMOTE Oversampling

![smote](https://github.com/hemalis/credit_risk_analysis/blob/main/images/SMOTE.png?raw=true)

_Balanced accuracy score:_ 0.6548711319915902

_Precision_ is **0.01** for high-risk loans and **1.00** for low-risk loans

_Recall_ is **0.62** for high-risk loans and **0.69** for low-risk loans

_Average Precision_ is **0.99** and _Average Recall_ is **0.69**

## 3. ClusterCentroids Undersampling

![under](https://github.com/hemalis/credit_risk_analysis/blob/main/images/Undersampling.png?raw=true)

_Balanced accuracy score:_ 0.5447339051023905

_Precision_ is **0.01** for high-risk loans and **1.00** for low-risk loans

_Recall_ is **0.69** for high-risk loans and **0.40** for low-risk loans

_Average Precision_ is **0.99** and _Average Recall_ is **0.40**

## 4. SMOTEEN

![SMOTEEN](https://github.com/hemalis/credit_risk_analysis/blob/main/images/SMOTEEN.png?raw=true)

_Balanced accuracy score:_ 0.6806030550435773

_Precision_ is **0.01** for high-risk loans and **1.00** for low-risk loans

_Recall_ is **0.80** for high-risk loans and **0.56** for low-risk loans

_Average Precision_ is **0.99** and _Average Recall_ is **0.56**

## 5. Balanced Random Forest Classifier

![BRF](https://github.com/hemalis/credit_risk_analysis/blob/main/images/BRF.png?raw=true)

_Balanced accuracy score:_ 0.7885466545953005

_Precision_ is **0.03** for high-risk loans and **1.00** for low-risk loans

_Recall_ is **0.70** for high-risk loans and **0.87** for low-risk loans

_Average Precision_ is **0.99** and _Average Recall_ is **0.87**

## 6. Easy Ensemble AdaBoost Classifier

![EasyEnsemble](https://github.com/hemalis/credit_risk_analysis/blob/main/images/EasyEnsemble.png?raw=true)

_Balanced accuracy score:_ 0.9316600714093861

_Precision_ is **0.09** for high-risk loans and **1.00** for low-risk loans

_Recall_ is **0.92** for high-risk loans and **0.94** for low-risk loans

_Average Precision_ is **0.99** and _Average Recall_ is **0.94**

# Summary

- Average Precision for all the results above is 0.99 which shows data is highly imbalanced and it's skewed. Most of the techniques works perfect for low-risk loans.

- SMOTE Oversampling in the case of this dataset does improve over the Random Oversampling where average recall is higher but SMOTE does have lower recall for high-risk loans.

- ClusterCentroids Undersampling doesn't work well with the dataset although is has higher precision for high-risk loans compared to SMOTE technique but recall is on lowest side.

- SMOTEEN provides smiliar results to SMOTE techniques with little higher balanced accuracy score. Average precision and recall are same as SMOTE.

- Balanced Random Forest Classifier algorithm works better then sampling techniques and it has higher average precision and recall compared to other techniques above. Recall for high-risk loan is still a concern for this model.

- Best model out of all six above is Easy Ensemble AdaBoost Classifier algorithm that trumps everything else in all categories with highest recall for both kind of loans and highest average precision and recalls that is 0.99 and 0.94.
