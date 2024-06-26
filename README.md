🚜 Predicting the Sale Price of Bulldozers using Machine Learning

Since we're trying to predict a number, we are dealing with a regression problem.

The data and evaluation metric we'll be using (root mean square log error or RMSLE) is from the Kaggle Bluebook for Bulldozers competition.

Since we already have a dataset, we'll approach the problem with the following machine learning modelling framework.

1. Problem Definition
For this dataset, the problem we're trying to solve, or better, the question we're trying to answer is,

How well can we predict the future sale price of a bulldozer, given its characteristics previous examples of how much similar bulldozers have been sold for?

2. Data
Looking at the dataset from Kaggle, we see it's a time series problem. This means there's a time attribute to dataset.

In this case, it's historical sales data of bulldozers. Including things like, model type, size, sale date and more.

There are 3 datasets:

  * 1. Train.csv - Historical bulldozer sales examples up to 2011 (close to 400,000 examples with 50+ different attributes, including SalePrice which is the target variable).
  * 2. Valid.csv - Historical bulldozer sales examples from January 1 2012 to April 30 2012   (close to 12,000 examples with the same attributes as Train.csv).
  * 3. Test.csv - Historical bulldozer sales examples from May 1 2012 to November 2012 (close to   12,000 examples but missing the SalePrice attribute, as this is what we'll be trying to     predict).

3. Evaluation
For this problem, Kaggle has set the evaluation metric to being root mean squared log error (RMSLE). As with many regression evaluations, the goal will be to get this value as low as possible.

To see how well our model is doing, we'll calculate the RMSLE and then compare our results to others on the Kaggle leaderboard.

4. Features
Features are different parts of the data. During this step, we'll want to start finding out what we can about the data.

One of the most common ways to do this, is to create a data dictionary.

For this dataset, Kaggle provide a data dictionary which contains information about what each attribute of the dataset means.

First, we'll import the dataset and start exploring. Since we know the evaluation metric we're trying to minimise, our first goal will be building a baseline model and seeing how it stacks up against the competition.
