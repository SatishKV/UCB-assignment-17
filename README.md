The Marketing activities of any organization can be carried over in different platforms however, marketing a Bank’s product requires more specific details and description. To carry out the same in a virtual platform, different methods of marketing and their practical applications were compared using the classifiers.

To run the application, the dataset from direct marketing campaigns (phone calls) of a Portuguese banking institution was used and the objective was to predict if the client will subscribe a term deposit. The performance comparison classifiers like Logistic Regression, Decision Trees, and Support Vector Machines were carried out using the data related to marketing bank products over the telephone. After understanding the task and features, data was encoded, and the prepared data was split into a train and test set.

1. Baseline & Simple Model: Logistic Regression Performance Classifier: Dummy Classifier used to fine baseline model that other classifiers should aim to beat. Accuracy score to aim - Baseline Model Score: 0.8865015780529255 To build a simple model on the template data, logistic regression was used. The accuracy of the model and its inference is given below in the reference (ROC Curve Comparison) Logistic Model Score: 0.9113862588006798
   ![image](https://github.com/SatishKV/UCB-assignment-17/assets/7441520/b2a32b62-6473-4be0-8bbd-46c660fcc497)
2. Comparison of Models without tuning: The performance of default Logistic Regression model was compared to default setting of three type KNN algorithm, Decision Tree, and SVM models and the findings were done on the Data Frame comprising Model, Train Time, Train Accuracy, Test Accuracy. The Model Comparison graph is given below where the regression model was compared with other models
3. ![image](https://github.com/SatishKV/UCB-assignment-17/assets/7441520/c176132a-3a74-49c4-9c9e-b080d9cff53e)
4. ![image](https://github.com/SatishKV/UCB-assignment-17/assets/7441520/e19270b4-490d-4f76-88b7-8a5acc7e5213)
With default setting Logistic Regression model perform well when considering combination trailing time, train & test accuracy, and AUC metric. KNN model though fast enough to train but test accuracy and AUC are falling behind. Decision tree test accuracy and AUC not better. Though SVM accuracies good but considering training time and slight down in AUC can be ranked as third among four models’ comparison.

3. Model Comparison with tuning / improvement: As part of improving/tuning model and compare different algorithm to choose between which algorithm to align with for model. Used GridSearch technique for hyperparameter tuning, cross validation and metrics adjustment. Comparison of all those algorithm-based models depicted as below both AUC & performance matrix.

Grid Search results with best param for four algorithms! Best parameters for Logistic Regression: {'clf__C': 1, 'clf__penalty': 'l2', 'clf__solver': 'liblinear'} Test accuracy of best model: 0.9114, Training time: 66.2672s Best parameters for KNN: {'clf__n_neighbors': 7} Test accuracy of best model: 0.9042, Training time: 27.1098s Best parameters for Decision Tree: {'clf__max_depth': 5} Test accuracy of best model: 0.9150, Training time: 9.1622s Best parameters for SVM: {'clf__C': 1, 'clf__kernel': 'rbf'} Test accuracy of best model: 0.9118, Training
![image](https://github.com/SatishKV/UCB-assignment-17/assets/7441520/ea6a7916-3f5d-40a7-a5ac-a74733a25cd8)
![image](https://github.com/SatishKV/UCB-assignment-17/assets/7441520/4abaa711-8d2f-475c-af6b-7be1b718a766)
![image](https://github.com/SatishKV/UCB-assignment-17/assets/7441520/0d2d9dad-b9bf-4905-87b3-b628d8b43f19)
![image](https://github.com/SatishKV/UCB-assignment-17/assets/7441520/aaac1762-7d62-4107-beb4-c9084c418cda)
Comparing all four algorithms, Decision Tree performing in terms of training time and accuracies but little lag in AUC. Decision Trees can struggle with imbalanced classes because they tend to Favor majority classes.

Conclusion Considering training accuracy, test accuracy, and AUC, Logistic Regression would be better model to align with nominal performance. KNN has very less AUC and SVM took almost 100 X times to perform, also not meant to handle large data set.

Impactful feature standpoint, correlation matrix (refer to correlation heatmap) and description provided that’s clear that having lengthy call with client with whom previous campaign attempted.
