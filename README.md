## Credit Risk Analysis Overview

In this challenge we will attempt to reinvent the weel, yes that's right will be trying to figure if people will actually pay back the money we lend them. An age old problem that dates all the way back to the creation of money, however we now have computers and machine learning to help us with this problem.We will use imbalanced-learn and scikit-learn libraries to build and evaluate machine learning models.

Analyze the credit card credit dataset from LendingClub, a peer-to-peer lending services company. Oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, compare two new ensemble machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

## Analysis Results
Our six models produced the following results:
-  RandomOverSampler  Oversampling Model
   * Balanced Accuracy Score:	0.6573
   * Precision Score: 		high_risk      0.01    low_risk       1.00    
   * Recall Score:              high_risk      0.71    low_risk       0.60
	
![image](https://user-images.githubusercontent.com/86337035/160262706-b135c565-7556-4ea9-9637-09088d573d23.png)


-  SMOTE_Oversampling Model
   * Balanced Accuracy Score:	0.6622
   * Precision Score: 		high_risk      0.01    low_risk       1.00    
   * Recall Score:              high_risk      0.63    low_risk       0.69

![image](https://user-images.githubusercontent.com/86337035/160262719-d893d6e0-11ac-4222-8c1a-6bba085b115f.png)


-  ClusterCentroids_Undersampling Model
   * Balanced Accuracy Score:	0.5443
   * Precision Score: 		high_risk      0.01    low_risk       1.00    
   * Recall Score:              high_risk      0.69    low_risk       0.40

![image](https://user-images.githubusercontent.com/86337035/160262730-30469186-cec2-475e-85db-877f11be6e6e.png)


-  SMOTEENN_Over/Undersampling Model
   * Balanced Accuracy Score:	0.6447
   * Precision Score: 		high_risk      0.01   low_risk       1.00    
   * Recall Score:              high_risk      0.72   low_risk       0.57

![image](https://user-images.githubusercontent.com/86337035/160262741-303a7634-fc3b-45aa-8f11-11531e41e027.png)


  - BalancedRandomForestClassifier_Ensemble Model

   * Balanced Accuracy Score:	0.7885
   * Precision Score: 		high_risk      0.03    low_risk       1.00    
   * Recall Score:     		high_risk      0.70    low_risk       0.87

![image](https://user-images.githubusercontent.com/86337035/160262749-e77e913f-bd80-4db4-a92a-c6c39f2efeac.png)


- EasyEnsembleClassifier_Ensemble Model
   * Balanced Accuracy Score:	0.9317
   * Precision Score: 		high_risk      0.09    low_risk       1.00    
   * Recall Score:    		high_risk      0.92    low_risk       0.94
				
![image](https://user-images.githubusercontent.com/86337035/160262756-9c0a0dc6-4f13-4abf-93a0-a937ff09a55f.png)


### Summary
The analysis shows that the ensemble model is better than the resampling model in all 3 catagories.
   * Worst Performing Model - ClusterCentroids undersampling
   * Best Performing Model - EasyEnsembleClassifier

Unfortunatley even with the relativley high level of success for the ensemble models the percsion scores for these models all still landed .10. This tells us that the model will give us far too many false positives if used in the real world, and if you are in the business of lending money it's probably not great if your model is turning away potentially good credit risks. You would be forced to loan money to low risk creditors and the scope of lending abilities would be limited greatly by a bad model. 
