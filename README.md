# Credit_Risk_Analysis

# Overview 
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, I used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Finally, I evaluated the performance of these models and made a written recommendation on whether they should be used to predict credit risk.

## Resources
* Data Source: LoanStats_2019Q1.csv
* Software: Python 3.9.12, Conda 22.9.0, Jupyter Notebook 6.4.12

# Results
## Deliverable 1: Use Resampling Models to Predict Credit Risk 
Using my knowledge of the imbalanced-learn and scikit-learn libraries, I evaluated three machine learning models by using resampling to determine which is better at predicting credit risk. First, I used the oversampling RandomOverSampler and SMOTE algorithms, and then I used the undersampling ClusterCentroids algorithm. Using these algorithms, I resampled the dataset, viewed the count of the target classes, trained a logistic regression classifier, calculated the balanced accuracy score, generated a confusion matrix, and generated a classification report.

1. Naive Random Oversampling

 * The balanced accuracy test it 65%, the precision for the high_risk has a very low positivity at 1% and the recall is 62%.
  
  <img width="718" alt="Naive Ramdom Oversampling" src="https://user-images.githubusercontent.com/106033535/195216973-3d551362-edad-4da7-b5aa-41ba89b655cd.png">

2. SMOTE Oversampling

 * The accuracy score is 66.2%, the precision for the high_risk loans has a low positvity again at 1% and recall is 69% overall.
  
  <img width="716" alt="SMOTE Oversampling" src="https://user-images.githubusercontent.com/106033535/195217437-3b392f48-033e-418e-8553-638faf95d30c.png">

3. Undersampling

  * Balanced accuracy score is 54% overall, the precision is at 99% and the recall is 40%.
  
  
  <img width="703" alt="undersampling" src="https://user-images.githubusercontent.com/106033535/195217536-33116783-acee-41aa-8eac-63d35fda2ebb.png">



## Deliverable 2: Use the SMOTEENN algorithm to Predict Credit Risk
Using my knowledge of the imbalanced-learn and scikit-learn libraries, I used a combinatorial approach of over- and undersampling with the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable  Using the SMOTEENN algorithm, I resampled the dataset, viewed the count of the target classes, trained a logistic regression classifier, calculated the balanced accuracy score, generated a confusion matrix, and generated a classification report.

4. Combination (Over and Under) Sampling

  * Balanced accuracy score is 64% the precision is 99% and the recall is 57% overall.
  
  
  <img width="706" alt="SMOTEENN" src="https://user-images.githubusercontent.com/106033535/195218112-749dfe1f-d5df-47b2-9f0d-9015ce5395ca.png">

  
## Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
Using my knowledge of the imblearn.ensemble library, I trained and compared two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. Using both algorithms, I resampled the dataset, viewed the count of the target classes, trained the ensemble classifier, calculated the balanced accuracy score, generated a confusion matrix, and generated a classification report.

5. Balanced Random Forest Classifier

  * The accuracy score is 74.2% the precision is 99% and the recall is 85%.
  
  
  <img width="722" alt="Balanced Random Forest Classifier" src="https://user-images.githubusercontent.com/106033535/195218340-12f049de-0a67-4bb9-a38b-a40f88b76810.png">
  
 6. Easy Ensemble AdaBoost Classifier
 
  * The accuracy score is 93% the precision is 99% and the recall is 94%.
  
  
<img width="718" alt="Easy Ensemble AdaBoost Classifier" src="https://user-images.githubusercontent.com/106033535/195218409-8273fc74-0740-4fe6-9589-850dcfee8a97.png">


# Summary
In the first four models I undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In the first four models othe accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Usually in the models you want a good balance of recall and precision. So I recommend the ensemble classifiers. It seems that the Easy Ensemble has the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.





  
