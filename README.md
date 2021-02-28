# Credit_Risk_Analysis
To apply Machine Learning models to analyze and predict credit card risk using datasets obtained from Lending Club (a peer to peer lending comapny). 

### Overview of the Credit_Risk_Analysis

The purpose of this analysis is to apply various Machine Learning models to analyze and predict credit card risk using datasets obtained from Lending Club (a peer to peer lending comapny). The dataset was oversampled using the RandomOverSampler and SMOTE algorithms, and undersampled using the ClusterCentroids algorithm. Various models were then used to predict the credit card risk with the results and performance of the models compared.

Specifically, this work invoved;

  1. Using Resampling Models to Predict Credit Risk
  2. Using the SMOTEENN Algorithm to Predict Credit Risk 
  3. Using Ensemble Classifiers to Predict Credit Risk 
  4. Generating a written report on the Credit Risk Analysis


To generate this analysis, I utilized the following resources;

  - Data Source: LoanStats_2019Q1.csv obtained from Lending Club 

  - Softwares: Python, Jupyter Notebook

### Results

Our reas of focus for the results of this analysis were;
1. Accuracy - which gives an indication of how often the classifier is correct
2. Precision - which gives an indication of how reliable a positive classification is
3. Recall (Sensitivity) - which is the ability of the classifier to find all positve samples

The following points enumerate the results of the different Machine Learning models that were applied in this analysis;

1. **Naive Random Oversampling**
 - Of a total of 101 high risk credit card applications, 69 were predicted correctly (True Positive) while 32 were predicted incorrectly (False Negative)
 - Of a total of 17,104 low risk credit card applications, 10,911 were predicted correctly (True Negative) while 6,193 were predicted incorrectly (False Positive)
 - Accuracy of the model was 66.05%
 - Precision for High Risk applications was 1% while Sensitivity (Recall) was 68%
 - Precision for Low Risk applications was 100% while Sensitivity (Recall) was 64%    

 The image below shows a snapshot of the Naive Random Oversampling method.


2. **SMOTE Oversampling**
 - Of a total of 101 high risk credit card applications, 62 were predicted correctly (True Positive) while 39 were predicted incorrectly (False Negative)
 - Of a total of 17,104 low risk credit card applications, 11,895 were predicted correctly (True Negative) while 5,209 were predicted incorrectly (False Positive)
 - Accuracy of the model was 65.47%
 - Precision for High Risk applications was 1% while Sensitivity (Recall) was 61%
 - Precision for Low Risk applications was 100% while Sensitivity (Recall) was 70%    

 The image below shows a snapshot of the SMOTE Oversampling method.


3. **Cluster Centroid - Undersampling**
 - Of a total of 101 high risk credit card applications, 70 were predicted correctly (True Positive) while 31 were predicted incorrectly (False Negative)
 - Of a total of 17,104 low risk credit card applications, 6,766 were predicted correctly (True Negative) while 10,338 were predicted incorrectly (False Positive)
 - Accuracy of the model was 54.43%
 - Precision for High Risk applications was 1% while Sensitivity (Recall) was 69%
 - Precision for Low Risk applications was 100% while Sensitivity (Recall) was 40%    

 The image below shows a snapshot of the Cluster Centroid Undersampling method.


4. **SMOTEENN - Combination (Over & Under)**
 - Of a total of 101 high risk credit card applications, 75 were predicted correctly (True Positive) while 26 were predicted incorrectly (False Negative)
 - Of a total of 17,104 low risk credit card applications, 10,130 were predicted correctly (True Negative) while 6,974 were predicted incorrectly (False Positive)
 - Accuracy of the model was 66.74%
 - Precision for High Risk applications was 1% while Sensitivity (Recall) was 74%
 - Precision for Low Risk applications was 100% while Sensitivity (Recall) was 59%    

 The image below shows a snapshot of the SMOTEENN combination method.


5. **Balanced Random Forest Classifier**
 - Of a total of 101 high risk credit card applications, 71 were predicted correctly (True Positive) while 30 were predicted incorrectly (False Negative)
 - Of a total of 17,104 low risk credit card applications, 14,951 were predicted correctly (True Negative) while 2,153 were predicted incorrectly (False Positive)
 - Accuracy of the model was 78.85%
 - Precision for High Risk applications was 3% while Sensitivity (Recall) was 70%
 - Precision for Low Risk applications was 100% while Sensitivity (Recall) was 87%    

 The image below shows a snapshot of the Balanced Random Forest Classifier.


6. **Easy Ensemble AdaBoost Classifier**
 - Of a total of 101 high risk credit card applications, 93 were predicted correctly (True Positive) while 8 were predicted incorrectly (False Negative)
 - Of a total of 17,104 low risk credit card applications, 16,121 were predicted correctly (True Negative) while 983 were predicted incorrectly (False Positive)
 - Accuracy of the model was 93.17%
 - Precision for High Risk applications was 9% while Sensitivity (Recall) was 92%
 - Precision for Low Risk applications was 100% while Sensitivity (Recall) was 94%    

 The image below shows a snapshot of the Easy Ensemble AdaBoost Classifier.



### Summary

For Lending Club, the objective of Machine Learning modelling for Credit Card risk analysis will be to try to identify a model that can always correctly predict high risk and low risk credit card applications. This way, the company will be able to maximize business opportunities (revenue) from correctly identified applications that are low risk while at thesame time significantly minimzing financial losses from correctly identified high risk applications.  

Summarizing the results generated by the 6 models, we could see that while the precision for low risk application were approximately 100% across the 6 models, the precision scores of the models across high risk applications showed that all the models returned very weak scores with the highest at 9% from the Easy Ensemble Classifier. The implication of this finding is that a significant chunk of the applications that are low risk were incorrectly classified as high risk, which may lead to lost business opportunities for Lending Club.

In thesame vein, a review of the Recall scores across the 6 models for high risk applications showed that the Easy Ensemble Classifier retruned the best score at 92% while thesame Easy Ensemble Classifier returned the best score of the 6 models with 94% for low risk applications

In terms of score accuracy, again, the Easy Ensemble returned the best score of 93.17% when compared to the accuracy scores of the other models.

Even though Easy Ensemble Classifier (when compared to other classifiers) showed the best scores (in terms of accuracy, precision & recall) across the high and low risk applications, I would still not recommend this classifier to Lending Club. This is because this model has a very weak precision score (9%) for high risk applications and this invariably mean that a significant chunk of the applications that are low risk were incorrectly classified as high risk, which would lead to lost business opportunities for Lending Club. 