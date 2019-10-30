# PyData Calgary Workshop Series: Hyperparameter Tuning 

## Getting started

Ensure you have the local dependencies installed:

```pip install -r requirements.txt```

## The data

We are using data from [Heart Disease UCI](https://papers.nips.cc/paper/4443-algorithms-for-hyper-parameter-optimization.pdf) from Kaggle. The dataset was chosen since it's quite small which will
help with evaluating expensive functions for SMBO. The dataset classifies patients for heart disease. 

## The problem

Given a simple decision tree classifier, employ several different hyperparameter optimization strategies to better understand the strategies for optimizing your own models. The steps
given below are guidelines/suggestions you could follow to play with the libraries. Follow whatever learning strategy works best for you. A (messy) example notebook is provided.

1. Create a random search to test different hyperparameters. Keep track of the best performing model. If desired, you can also implement exhausitve search
   1. You can roll your own, use hyperopt, use sklearn RandomSearchCV, or anything else that tickles your fancy
2. Implement a bayesian method. Most examples use hyperopt which is a [Tree Parzen Estimator](https://papers.nips.cc/paper/4443-algorithms-for-hyper-parameter-optimization.pdf), but you can also use a gaussian process or random forest based approach if you're a maverick
3. Plot the differences in hyperparameters selected from random search and bayesian optimization
4. Plot the change in hyperparameters over time from bayesian optimization 
5. If you somehow have managed to finish all of this in 2 hours, implement hyperparameter optimization using genetic algorithms and compare that to bayesian optimization

## Additional Resources

An excellent reference going step by step through the optimiation of a difficult problem, epxloring the impact and usage of various optimization techniques was created by
Dr. Muir from CalgaryR and can be found [Here](https://rpubs.com/Alastair/535436)

A large amount of the code for this notebook was ripped from the following resources:

https://github.com/WillKoehrsen/hyperparameter-optimization/blob/master/Introduction%20to%20Bayesian%20Optimization%20with%20Hyperopt.ipynb
https://towardsdatascience.com/an-example-of-hyperparameter-optimization-on-xgboost-lightgbm-and-catboost-using-hyperopt-12bc41a271e