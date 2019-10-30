# Ensemble Package

Package for Ensemble of Machine Learning Models
-----------------------------------------------
The motivation was to incorporate the various techniques described into a single python package. The current version of the package has the power to perform weighted averaging, and build stacking and blending models for binary classification. The other ensembling techniques will be incorporated in the future. The package enables data encoding, the desired data on which the user wishes to classify the data, can be encoded in many different ways like label encoding (categorical encoding), one hot encoding, sum encoding, polynomial encoding, backward difference encoding, helmert encoding, and hashing encoding. The encoded data will then be used to train the base models. The package provides the user with the ability to build a number of base models such as Gradient Boosting (XGBoost), Multi Layer Perceptron, Random Forest Classifier, Decision Tree, Linear Regression, Logistic Regression. The user can build any or all the base models with default parameter values, change the parameter values or provide a list of parameter values to perform hyper parameter optimistaion (Using Hyperopt and Grid Search) and identify the optimum parameter values. Once the desired parameter values have been obtained the respective base models will be trained. Upon training the models, the trained models are used to obtain predictions on the cross validation data, these predictions obtained from the base models will be used to construct a data frame, which will be used to train the stacking and blending models, and perform weighted averaging.

Once the base models have been trained the user can select which ensembling technique to use. The dataframe of predictions will be used to perform weighted averaging, the same dataframe will be used to train the stacking model, for training the blending model the dataframe of predictions will be appended with the cross validation data. To train the ensemble models the algorithm or classifier which will be used can be any of the algorithms/classifiers provided for the training of the base models. For testing the stacking and blending models we can hold out a test set which can be used to examine how well these ensemble models perform, wether they overfit, underfit, provide better performance than the base models.

# Installation

[ **pip install ensembles** ]

*Dependecies*

* functools.
* numpy.
* sklearn.
* keras.
* xgboost [github link](https://github.com/dmlc/xgboost).
* joblib [github link](https://github.com/joblib/joblib).
* hyperopt [github link](https://github.com/hyperopt/hyperopt).
* category_encoders [github link](https://github.com/wdm0006/categorical_encoding).

#Documentation

Changes are being made to some parts of the documentation.
The documentation for the package is hosted [here](http://pythonhosted.org/ensembles)

# Base Models

* Linear Regression.
* Gradient Boosting (XGBoost). 
* Random Forest Classifier.
* Decision Tree.
* Logistic Regression.

# Ensemble Models

* Blending.
* Stacking.
* Weighted Average.

# Key Features

* The option to perform hyper parameter optimisation for any of the models (hyperopt and gridsearch)
* Running the models in parallel during training and testing (joblib).

# Examples

* An explanation of how the package works is in the ensembles/examples folder

# License

MIT License
