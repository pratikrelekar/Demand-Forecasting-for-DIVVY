# Demand-Forecasting-for-DIVVY


This repository contains code for bike demand forecasting using various models and techniques. The goal of this project is to predict the demand for registered and casual customers, as well as the total demand for bikes.

Data

The dataset used for the analysis is stored in the file "BikeDemandDaily.csv". It includes information about daily bike demand, weather conditions, and other relevant variables.

Code Structure

The code is organized into several parts, each focusing on a specific aspect of demand forecasting.

Data Exploration and Visualization:
The initial code segment loads the dataset using pandas and performs some initial data exploration.
It includes visualizations to compare the daily demand for registered and casual customers, as well as scatter plots to examine the relationships between demand and weather variables such as mean temperature, humidity, wind speed, and standard deviation of wind speed.
Disaggregated Demand Forecasting:
This part focuses on forecasting the demand for registered and casual customers separately.
It applies the LASSO (Least Absolute Shrinkage and Selection Operator) regression technique to select relevant features and create models for each type of demand.
The code splits the dataset into training and testing sets, performs cross-validation to find the optimal penalty parameter for LASSO, constructs the final LASSO models, and predicts the demand on the testing set.
The Root Mean Squared Error (RMSE) is calculated to evaluate the performance of the models.
Time Series Prediction - ARMA Models:
This section applies Auto Regressive Moving Average (ARMA) models to the residuals obtained from the LASSO models.
The residuals are used to assess the autocorrelation of the demand time series.
ARMA(2,2) models are then fitted to the residuals to capture any remaining patterns in the data.
The ARMA models are used to predict the demand for registered and casual customers on the testing set.
The RMSE is calculated to evaluate the accuracy of the ARMA models.
Aggregate Demand Forecasting:
This part focuses on forecasting the total demand for bikes by aggregating the demand for registered and casual customers.
It applies the LASSO regression technique to select relevant features and creates a model for total demand.
The code compares the performance of the LASSO model with an ARMA(2,2) time series model on the testing set.
The RMSE is calculated to evaluate the accuracy of the models.
Results

The analysis provides insights into the factors influencing bike demand and compares different modeling approaches for forecasting registered, casual, and total demand.

The graphical comparisons and scatter plots reveal relationships between demand and weather variables, highlighting the impact of mean temperature on demand.
Box plots show the differences in demand during holidays and on different days of the week, indicating the preferences of registered and casual customers.
The LASSO models help identify relevant features and provide predictions for registered and casual demand. The models are evaluated using RMSE, and the optimal penalties for LASSO are reported.
The ARMA models capture any remaining patterns in the demand time series, and their predictions are compared to the LASSO models.
The aggregate demand forecasting compares the performance of LASSO and ARMA models for predicting total demand.
The results demonstrate the effectiveness of the different forecasting approaches and provide insights into the factors influencing bike demand. The RMSE values indicate the accuracy of the models in predicting demand.

Please refer to the code and comments in the files for detailed explanations of each step in the analysis.

Note: This README provides a brief overview of the project. For a more comprehensive understanding, please refer to the code files and associated comments.
