# Exo Planet Exploration 


Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, machine learning models, capable of classifying candidate exoplanets from the raw dataset are created as described below:

  * The dataset is preprocessed, prior to fitting the model.
  * Feature selection is performed and unnecessary features are removed (features whose importance was determined to be less than 0.01% by running the decision tree alogrithm).
  * MinMaxScaler was used to scale the numerical data.
  * Separated the data into training and testing data.
  * Used GridSearch to hyper tune model parameters.
  * Tuned and compared three different classifiers.
  
### Results

Random Forest model is better than Support Vector Machine, even without hyper tuning the parameters with GridSearchCV. Of all the models considered (SVM, Random Forest and Gradient Boosting). Gradient Boosting model yielded highest accuracy of 91%.

SVC 
---
                       precision   recall  f1-score   support

     CANDIDATE            0.76      0.61      0.68       422
     CONFIRMED            0.69      0.79      0.74       450
     FALSE POSITIVE       0.99      1.00      0.99       876

     accuracy                                 0.85      1748
     macro avg            0.81      0.80      0.80      1748
     weighted avg         0.85      0.85      0.85      1748


SVC with hyper tuning
-----------------------

                        precision   recall   f1-score   support

     CANDIDATE            0.84      0.71      0.77       422
     CONFIRMED            0.76      0.86      0.80       450
     FALSE POSITIVE       0.99      1.00      0.99       876

     accuracy                                 0.89      1748
     macro avg            0.86      0.85      0.86      1748
     weighted avg         0.89      0.89      0.89      1748

  
  
Random Forest
---------------

                        precision    recall  f1-score   support

     CANDIDATE            0.74      0.83      0.78       373
     CONFIRMED            0.84      0.81      0.82       472
     FALSE POSITIVE       1.00      0.97      0.98       903

     accuracy                                 0.90      1748
     macro avg            0.86      0.87      0.86      1748
     weighted avg         0.90      0.90      0.90      1748


Random Forest with hyper tuning
--------------------------------

                        precision    recall  f1-score   support

     CANDIDATE            0.84      0.76      0.80       422
     CONFIRMED            0.82      0.86      0.84       450
     FALSE POSITIVE       0.97      1.00      0.99       876

     accuracy                                 0.90      1748
     macro avg            0.88      0.87      0.87      1748
     weighted avg         0.90      0.90      0.90      1748

     
Gradient Boosting
------------------

                        precision    recall  f1-score   support

     CANDIDATE            0.85      0.79      0.82       422
     CONFIRMED            0.82      0.85      0.83       450
     FALSE POSITIVE       0.99      1.00      0.99       876

     accuracy                                 0.91      1748
     macro avg            0.88      0.88      0.88      1748
     weighted avg         0.91      0.91      0.91      1748


Gradient Boosting with hypertuning
------------------------------------

                         precision    recall  f1-score   support

     CANDIDATE             0.84      0.80      0.82       422
     CONFIRMED             0.82      0.85      0.83       450
     FALSE POSITIVE        0.99      1.00      1.00       876

     accuracy                                  0.91      1748
     macro avg             0.88      0.88      0.88      1748
     weighted avg          0.91      0.91      0.91      1748

