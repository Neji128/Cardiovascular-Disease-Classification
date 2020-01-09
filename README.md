
# Cardiovascular Disease Classification: Module 5 Final Project


## Introduction:

A diagnostician is requesting assistance in refining their team's ability to identify cardiovascular disease (CD) using data they gathered from 70,000 patients. We have been tasked with exploring the data and creating a classification model meant to predict CD within the patient population. The purpose of the present work is to supplement existing diagnostic techniques employed in medical sciences in addition to examining the quality of the data collected. 
   
## Objectives:

* Development of a CD classification model 
* Explore risk factor contributions to CD
* Explore risk factor interactions

## Conclusions:

* Cholesterol and physical activity interact in a significant fashion when predicting CD. 
* The XGBoost model for the BMI condition the best perfroming for predicting CD based on the present dataset.
    * All factors used to predict CD within this condition were significant predictors unlike the height/weight condition.
    * Converting some binary variables to continuous variables may provide additional insight and contribute to a more accurate model. Specifics are included within the included notebook and slide deck concerning which variables to target this way.
    * Model should not be explicitly used as a diagnostic tool and should instead be used as a training diagnostic training tool to guide resident physicians and emerging medical clnicians in predicting CD.
    
## Function Clarification

classifier_generator(df, y, X, clf_list)

* clf_list needs to be a list of classifiers with random_state uniformally defined. An example is included below:
    * clf_list = [XGBClassifier(random_state=0), LogisticRegression(random_state=0), 
            AdaBoostClassifier(random_state=0), GradientBoostingClassifier(random_state=0)]
* The train-test-split is included within the function. Be sure to keep the random states uniform across classifiers and train-test-split

## Dataset Source

https://www.kaggle.com/sulianova/cardiovascular-disease-dataset

## The Deliverables

* classification jupyter notebook
* slide deck
* audio/visual walkthrough
* cardio_train_csv

## Packages Needed

* pandas
* scipy 
* stats
    * numpy 
* matplotlib.pyplot
* matplotlib.style
* seaborn
* warnings
* statsmodels.api as sm
* statsmodels.formula.api
    * ols
* sklearn.model_selection 
    * train_test_split
    * GridSearchCV
* sklearn.linear_model
    * LogisticRegression
* sklearn.metrics
    * accuracy_score
    * roc_curve
    * auc
* xgboost
    * XGBClassifier
* yellowbrick.classifier
    * ConfusionMatrix
* sklearn.ensemble
    * AdaBoostClassifier
    * GradientBoostingClassifier


## Blog Post Link

https://neji128.github.io/cardiovascular_health