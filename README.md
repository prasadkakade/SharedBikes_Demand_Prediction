# SharedBikes_Demand_Prediction

## Run the code file 'BooomBikes.ipynb' with input file as 'day.csv'

## Problem Statement -
Bike-sharing system company has a dataset containing count of shared bikes. It wishes to use the data to understand the factors (holiday. year, weekday, etc) affecting the demand  for these shared bikes in the American market.

Essentially, the company wants to know -
1. Which variables are significant in predicting the demand for shared bikes.
2. How well those variables describe the bike demands

## Methodology - 
1. Read the file "day.csv"
2. Perform EDA on the data
3. Prepare the datset for training (Dummy variables creation)
4. Splitting the training and test data, use scaler to transform the data
5. Build a linear model
6. Use RFE to select top features, use VIF and P-value to find features having high importance.
7. Predict on test data and compare the results

## Results - 
Linear Regression model gave following equation
#### count = 0.235\*year - 0.086\*holiday + 0.476\*temp - 0.135\*windspeed - 0.103\*pring + 0.050\*winter - 0.256\*ws 3 - 0.062\*july + 0.049\*sep + 0.204\*constant 

So,top 3 features having higher impact on count of shared bikes are - 
1) yr 
2) temp 
3) ws_3 (Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds)
