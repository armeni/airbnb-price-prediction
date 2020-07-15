# Airbnb Price Prediction

## Problem description
Airbnb (www.airbnb.com) is a hospitality company that runs an online marketplace for renting and leasing short-term lodging. It is interested in developing a pricing service for its users that will compute a recommended price based on the features of a listing. As a consultant working for a data analytics company, you are approached by Airbnb to develop a model for predicting nightly prices of Airbnb listings based on state-of-art techniques from statistical machine learning.
You are provided with a dataset containing detailed information on a number of existing Airbnb listings in Melbourne, Australia. As part of the contract, you are asked to write a report according to the instructions given below. The client will use a test set to evaluate your work.

## Data Description 
Each row corresponds to a separate Airbnb listing in Melbourne. As a consequence of using real data, a detailed description of all the variables is not available, and there may be entry errors. However, the names of the variables are self-explanatory. The first column in the data provides an identifier for each listing and is included to comply with the Kaggle format. It should not be used as a predictor in the analysis. The response variable, price, is the second column in the training dataset. It gives the dollar price per night for each listing. Variables security_deposit, cleaning_fee and extra_people are also measured in dollars and correspond to surcharges. Variables latitude and longitude specify the geographic location of each property. Several variables are Boolean, with the word true recorded as “t” and false recorded as “f”.

## Methodology
To predict the price of Airbnb housing in Melbourne, the approach of sequential use of a set of models from simple to more complex, as well as an assessment of each subsequent model relative to the previous one, was chosen. 
Selected models: 
- Linear Regression, Ridge, Lasso, Elastic Net
- k-nearest neighbors method 
- Random Forest
- Gradient Boosting methods: XGBoost, CatBoost, LightGBM 
At the initial stage, the quality of the model is also compared with respect to the application of methods for processing missing values: zero, average, and median.

The models quality is evaluated using 5-folds cross-validation according to the RMSE metric. For gradient boosting models, 10% of the data is additionally allocated for validation and the search for the moment of early stopping of training in order to maintain the highest level of generalizing ability.
