# machine_learning_homework
## Resampling Analysis and Modeling
In this analysis, several types of data resampling were used on the existing loan statistical data set.  
These included: 
1. Naive Random Oversampling
2. SMOTE Oversampling
3. Undersampling
4. SMOTEEN Combination (Over and Under) Sampling 

Once the data was resampled, given the selected method, the model was fit to the training data using a logistic regression model. The balanced accuracy score, confusion matrix, and imbalanced classification report were obtained for all datasets in this model type.

Please note in the following results, the negative(0) outcome refers to a loan status - 'high risk' and the positive(1) outcome refers to a loan status - 'low risk'.

### The following are important conclusions on data resampling:

* Which model had the best balanced accuracy score?

    The logistic regression model produced with the Naive Random Oversampled data had the best balanced accuracy score at 0.661. This model had the highest balanced accuracy score. SMOTE oversampling ( Balanced Accuracy Score=0.615) and SMOTEENN (Over-Under Sampling) (Balanced Accuracy Score=0.613) were the fairly close to eachother in behavior for balanced accuracy and came in 2nd best. Undersampling (Balanced Accuracy Score=0.512) was the worst performing balanced accuracy score.

* Which model had the best recall score?

    Again, the model fit on Naive Random Oversampled data had the best recall score overall for both negative(0) and positive(1) outcomes of 0.66 and 0.67 respectively. The model fit on SMOTE (Recall=0.55/0.68) had a slightly higher score than the Random Oversampled model, but only for the positive outcomes. It didn't perform well on the negative ones for recall. Similarly, the SMOTEEN based model (Recall=0.68/0.55) had a reverse scenario where it did just a bit better at recall for negative results, but much worse at positive recall. Finally, the Undersampling based model (Recall=0.57/0.45) did poorly for recall for both negative and positive outcomes.


* Which model had the best geometric mean score?

    The logistic regression model fit with the Naive Random Oversampling data also had the best geometric mean score of 0.66. The models based on SMOTE Oversampling and SMOTEENN (Over-Under Sampling) performed the same on this metric with a geometric mean score of 0.61. The worst performing geometric mean score was for the Undersampling based model, which scored only 0.51.

Overall, it could be concluded that for this particular set of loan statistical data. The Naive Random Oversampling of the existing data produced the best fit model with the highest balanced accuracy score, best recall score, and best geometric mean score. The other models fit to various types of resampled data were alright, but they definitely did not perform as well. SMOTE Oversampling and SMOTEENN (Over-Under Sampling) came close to the performance of the Naive Random Oversampling, whereas Undersampling did not perform well.

## Ensemble Learning and Modeling
In this analysis, two types of data classification models were used on the existing loan statistical data set.  
These included: 
1. Balanced Random Forest Classifier
2. Easy Ensemble AdaBoost Classifier

Please note in the following results, the negative(0) outcome refers to a loan status - 'high risk' and the positive(1) outcome refers to a loan status - 'low risk'.

### The following are important conclusions on ensemble learning:

* Which model had the best balanced accuracy score?

The Easy Ensemble AdaBoost Classifier has the best balanced accuracy score of 0.91. This is a very good score as a balanced accuracy score of 1 is a perfect score. The Random Forest Classifier did alrigh, but had a lower balanced accuracy score of 0.661.

* Which model had the best recall score? 

    The easy Ensemble AdaBoost Classifier had the best recall score with 0.84 recall for the negative(0) outcomes and 0.98 for the positive(1) outcomes. This is a very good recall for both types of classification. Again the Random Forest Classifier was not as strong. However, the Random Forest did have a recall of 1 for positive(1) outcomes which is really good, but it had a poor recall of only 0.32 for negative(0) outcomes.
* Which model had the best geometric mean score?

    The Easy Ensemble AdaBoost Classifer had the best geometric mean score of 0.91. The Random Forest Classifier had a geometric mean score of 0.57, so not as good.
* What are the top three features?
The top features by importance are:
    1. Total_Rec_Prncp (Total Recent Principle) with importance score of 0.08. Accounts for 8% of influence.
    2. Total_Pymt_Inv (Total Payment Inv) with importance score of 0.07. Accounts for 7% of influence.
    3. Total_Rec_Int (Total Recent Interest) with importance score of 0.06. Accounts for 6% of influence.
Thus, the top 3 features account for 21% of the influence on the result.

Based on the results it is clear that the preferred model for fitting and predicting based on this data set would be the Easy Ensemble AdaBoost Classifier.