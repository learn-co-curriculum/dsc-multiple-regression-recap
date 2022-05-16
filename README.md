# Multiple Linear Regression - Recap

## Introduction

In this section you extended your knowledge of building regression models by adding additional predictive variables, including categorical variables.

## Key Takeaways

* ***Multiple linear regression*** builds on simple linear regression
  * Instead of finding just one coefficient and one intercept, multiple regression finds a coefficient for each independent variable (predictor)
  * The coefficients are not the same if you build several different simple linear regression models vs. using those same predictors in a single multiple regression model. This is because a multiple regression model is "***controlling for***" the other variables.
    * A randomized controlled experiment is the gold standard way to control for confounding variables, but multiple regression is an alternative strategy when an experiment is not possible
* In an inferential context, we typically use ***StatsModels*** to build multiple regression models, just like we did for simple regression models
  * Another library that can be used for linear regression is ***scikit-learn***. This is mostly relevant for predictive modeling (machine learning) because it doesn't calculate p-values for coefficients
* There are some problems with R-Squared (coefficient of determination) for evaluating multiple regression models
  * R-Squared will only ever increase as we add more features. ***Adjusted R-Squared*** accounts for the number of features and is a better metric for multiple regression
  * Proportion of variance explained is not intuitive for stakeholders. ***Error-based metrics*** such as mean absolute error (MAE) and root mean squared error (RMSE) are helpful tools to express how incorrect the model is in an average prediction
* Now that we have the ability to use multiple features in our regression models, we can use ***categorical features***
  * Categorical features must be ***preprocessed*** before they can be used in linear regression models
  * Specifically we used ***one-hot encoding*** to create dummy variables (1s or 0s) representing each category
  * In order to avoid the ***dummy variable trap*** we need to drop one of the dummy variable columns. Whichever column is dropped becomes the ***reference category***, where all other category coefficients are compared to this category.
