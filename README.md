# Credit Risk Analysis
## Overview of the analysis
Selling a credit card for a bank is always profitable, however, there is a high risk involved in this fruitful business as well. 🍇
In this project, we tried to determine how risky is credit card sales by using machine learning. We used a supervised learning technique. That means, we used data that contains customers' previous behaviours and status and tried to determine if there is low risk or high risk for the banking industry.

One of the obstacles was the ratio of good loans to risky loans. Because the good loan number was very high, we had to use oversample and undersample techniques to balance the data risk volume.

And lastly, we tried to predict the credit risk by using BalanceRandomFOrestClassifier and EasyEnsembleClassifier.
## Results
### Interpretation of Balanced Accuracy Scores and the Precision and Recall Scores

#### RANDOM OVERSAMPLING

![image](https://user-images.githubusercontent.com/98247252/176347321-085d2cee-73e6-4be8-bd2f-58d56a34b557.png)

💳 _Accuracy Score_ = Accuracy score is the Percentage of predictions that is correct, in that case, True Positives and True Negatives. only 64% of the time is predicted correctly, which is low.

💳 _Precision_: That means how reliable our positive classification is. We successfully determined the low-risk applicants, however, Random Oversampling failed to detect the High-Risk Applicants.

💳 _Recall_: We use it the positive outcome us crucial such as (Real High Risk, or real cancer disease). The recall is the ability of the classifier to find positive samples. In this case, high risk is 72% and low risk is 57%. bot result is not satisfying.

#### SMOTE OVERSAMPLING
![image](https://user-images.githubusercontent.com/98247252/176702977-21d22763-0238-4694-8558-f263afcec77b.png)

💳 _Accuracy Score_: Smote Oversampling only 64% of the time predicted the actual High Risk and actual Low Risk. 

💳 _Precision_: The model is very successful the determining Low-Risk applicants however it is not successful to determine high-risk applicants

💳 _Recall_: model's ability to find low-risk applicants is 69%, and high-risk applicants are 63%. this result for hight risk applicants is slightly better than the Random Oversampling technique.

#### UNDERSAMPLING

![image](https://user-images.githubusercontent.com/98247252/176706790-3aa20293-e0e0-442a-b0df-7375017a5017.png)

💳 _Accuracy Score_: Undersampling technique only 54% of the time predicted the actual High Risk and actual Low Lisk.

💳 _Precision_:  The model is very successful the determining Low-Risk applicants however it is not successful to determine high-risk applicants.

💳 _Recall_: Reliability positive results for High Risk 69%,  for Low Risk is 40%. This model is more sensitive to cath High-Risk applicants.

#### COMBINATION (OVER and UNDER) SAMPLING

![image](https://user-images.githubusercontent.com/98247252/176710097-2cac645f-148d-4d71-9532-ccb44e0b382d.png)

💳 _Accuracy Score_: The combination Sampling technique only 64% of the time predicted the actual High Risk and actual Low Lisk.

💳 _Precision_:  The model is very successful the determining Low-Risk applicants however it is not successful to determine high-risk applicants.

💳 _Recall_: Reliability Positive results for High Risk 72%,  for Low Risk is 40%. This model is more sensitive to cath High-Risk applicants.

#### BALANCE RANDOM FOREST CLASSIFIER

![image](https://user-images.githubusercontent.com/98247252/176715142-fad761fd-14ab-489c-8aad-b2fd70a87e3d.png)

💳 _Accuracy Score_: Balance Random Forest Classifier technique 79% of the time predicted the actual High Risk and actual Low Lisk.

💳 _Precision_:  The model is very successful the determining Low-Risk applicants however it is not successful to determine high-risk applicants.

💳 _Recall_: Reliability; Positive results for High Risk 70%,  for Low Risk is 87%. This model is relatively sensitive and successful in determining High-Risk applicants.

#### EASY EMSEMBLE ADABOOST CLASSIFIER

![image](https://user-images.githubusercontent.com/98247252/176716243-5ac5a180-6421-4c8e-96f3-456000b385f1.png)

💳 _Accuracy Score_: Easy Emsemble Adaboost Classifier technique 93% of the time predicted the actual High Risk and actual Low Lisk.

💳 _Precision_: Precision on high risk is still low. That means we have a significant number of false positives

💳 _Recall_: Reliability; Positive results for High Risk 94%,  for Low Risk is 92%. This model is very sensitive and successful in determining High Risk and Low-Risk applicants.

## Summary:

Prediction of credit application in High Risk and Low Risk is important. If a certain application is a low risk but we predicted it as high risk, this can always be corrected by the Bank. However, accuracy and sensitivity in predicting Actual High Risk (True Negative) are vital. Here we wanted to determine all True Positives and True Negatives. Therefore Sensitivity (RECALL) is very important for us.

According to our test results, the technique of ensemble learning gives better results than under or oversampling(and their kinds). Ensemble learning (including Random Forest) works with many decision trees and collects all the from many "Weak Leaners" as a result our prediction, accuracy or reliability becomes better.

Recommendation: Easy Emsemble Adaboots Classifier technique seems to perform best among the six techniques however the Precision rate is still low for High-Risk applications!
