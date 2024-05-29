# Stock Price Prediction Model

This project contains multiple stock price prediction models. So far the only models we have made are Random Forest Classifiers and Gradient Boosting Classifiers from the SK-Learn library in Python.

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Data](#data)
- [Models](#models)
  - [Random Forest Classifier](#random-forest-classifier)
  - [Gradient Boost Classifier](#gradient-boost-classifier)

## Introduction

**The only stock in consideration for now is the SPY index fund. This is for simplicity and consistency. Index funds are also generally more predictable.**

This project aims to predict stock price movements using machine learning techniques. 
Specifically, we employ Random Forest and Gradient Boost classifiers to predict whether 
the stock price will go up or down as we are not so concern with the exact value it will be.


## Installation

To get started, make sure you have jupyter notebook installed and available on your machine. 
Then, pick the python notebook that corresponds with the algorithm you would like to use.

```bash
https://github.com/sunnypatel314/StockPricePredictionML.git
cd StockPricePredictionML
```

## Data
The data is collected from Python's yfinance library which directly gathers stock data from yahoo finance. 
The Pandas library in Python is then used to preprocess and clean data, and extract useful features from the data.
The features and data might differ from model to model.

## Models

### Random Forest / Gradient Boosting 
The features we are aiming to extract are close ratios and trends for the last **2, 5, 10, 30, 60, 250, and 1000 trading days**.
The Random Forest Classifier will attempt to predict the directionality (up or down) of the stock based on all of the features gathered from the data.

For Random Forest Classification, data scaling and normalization is generally not required and tree-algorithms in machine learning 
are considering data in its raw form. For Gradient Boosting, however, scaling is required. The model at its best has achieved **56% accuracy** on data it has not seen (testing data), which is good considering the 
unpredictable nature of stock market prices. There is a function in the python notebook called **"simulate_paper_trading"**, which compares the profit you could have 
achieved if you followed the predictor compared to if you blindly bought and sold everyday. Just to be clear, the function mentioned only considers 
testing data (data it has never seen before) to make sure the model does not have an unfair advantage.

For evaluation, the standard precision score is applied to the models. The formula is as followed:

![image](https://github.com/sunnypatel314/StockPricePredictionML/assets/110628037/4a9cd458-8743-47ec-98f4-9c27ad800798)


