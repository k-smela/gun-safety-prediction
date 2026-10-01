# Predictive Modeling of Gun Safety Laws and Outcomes

Team project — Statistical Methods course, Colorado College, 2024.

## Overview
This project applies statistical classification and regression methods to 
study relationships between a range of predictors and several gun safety 
outcomes. The dataset was cleaned to remove null observations and 
partitioned into training and testing sets.

**Classification:** Five models — logistic regression, LASSO, ridge, 
Naive Bayes, and KNN — were each fit to predict the presence or absence of 
a given law (e.g., universal background checks, shall-carry laws, gun 
permit requirements). Predictors for the logistic regression model were 
selected via backward stepwise selection, and models were compared using 
the area under the ROC curve. The best-performing model overall was the 
LASSO classification model predicting permit-to-purchase laws, achieving 
an area under the ROC curve of 0.9950.

**Regression:** Four numerical outcomes — murder rate, violent crime rate, 
robbery rate, and household firearm ratio (HFR) — were each predicted 
using six model types: linear regression (Gaussian, identity link), 
Gaussian with a log link, Gaussian with a square-root link, Gamma with a 
log link, Gamma with a square-root link, and KNN (used for predictive 
comparison rather than interpretation). Poisson GLMs were excluded since 
none of the response rates are whole-number counts. Backward selection was 
used to reduce predictors for each model, and LASSO selection was 
additionally run for each response variable across GLM types. Models were 
compared using test mean squared error.

## Contents
- `classification_models.html` — R code (rendered from R Markdown) fitting 
  and comparing the five classification models predicting law presence/absence
- `violent_crime_regression_models.html` — R code (rendered from R Markdown) 
  fitting and comparing regression models predicting violent crime rate
- `final_report.pdf`— Full written-up report of project findings, including visualizations.

## Skills Demonstrated
- Data cleaning and train/test partitioning
- Classification modeling: logistic regression, LASSO, ridge, Naive Bayes, KNN
- Regression modeling: generalized linear models across multiple 
  distributions and link functions
- Variable selection: backward stepwise selection, LASSO
- Model evaluation and comparison: area under the ROC curve 
  (classification), test mean squared error (regression)
- Statistical reasoning in distribution/link choice (e.g., excluding 
  Poisson regression based on data structure)

## Tools
R, R Markdown
