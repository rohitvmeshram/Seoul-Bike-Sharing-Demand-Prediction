# Seoul-Bike-Sharing-Demand-Prediction
The goal of this project is to combine the historical bike usage patterns with the weather data to forecast bike rental demand. The data set consists of hourly rental data spanning two years.
Exploratory Data Analysis is done on the dataset and compare the target variable with the other variables to find the distribution of graph. We look for null values which were not found and outliers and appropriately modify them by z-score. We also perform correlation analysis to extract out the important and relevant feature from dataset and later perform train test split to train the model.
The main objective is to build a predictive model, which could help to train a model to predict the number of bike rentals of the year given the weather conditions.  This would in turn help to predicting quickly and efficiently.

#1.	Problem statement :

The main objective is to build a predictive model, which could help to train a model to predict the number of bike rentals of the year given the weather conditions.  This would in turn help to predicting quickly and efficiently.
The dataset contain following columns : 
•	Date : year-month-day
•	Rented Bike count - Count of bikes rented at each hour
•	Hour - Hour of the day
•	Temperature-Temperature in Celsius
•	Humidity - %
•	Windspeed - m/s
•	Visibility - 10m
•	Dew point temperature - Celsius
•	Solar radiation - MJ/m2
•	Rainfall - mm
•	Snowfall - cm
•	Seasons - Winter, Spring, Summer, Autumn
•	Holiday - Holiday/No holiday
•	Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)

#	Steps involved :

The following steps are involved in the project
1.	Exploratory Data Analysis : 
After loading and reading the dataset in notebook, we performed EDA. Comparing target variable which is bike rentals counts with other independent variables. This process helped us figuring out various aspects and relationships among the target and the independent variables and also we observed the distribution of variables. It gave us a better idea that how feature behaves with the target variable.
2.	Null values Treatment and Outliers :
Dataset contains a no null values to disturb the accuracy but outliers are present which can disturb the accuracy. So Again,  we use z-score to remove outliers.

3.	Numerical and categorical Features : With the help of exploratory data analysis we analyzed the categorical as well as numerical features in the dataset.

4.	One hot encoding :
In this dataset some categorical variables like seasons, holiday and function day, we change it with numerical database.

5.	Correlation Analysis :
We plot the heatmap to find  the correlation between both dependent variable and independent variables.

6.	Train test Split :
In train test split we take x as dependent variables and y take as independent variable then train the model.

7.	Models :
We uses 11 modeling  to train the data and for predicting the accuracy, RMS and R2.  
1.	Linear regression
2.	Lasso regression
3.	Ridge regression
4.	Elastic net
5.	Polynomial regression
6.	KNN and Tree based model
7.	Random forest
8.	Gradient boosting
9.	Extreme gradient boosting
10.	Catboost
11.	LightBGM

#	Conclusions : 
1. In holiday or non-working days there is demands in rented bikes.
2.  There is a surge of high demand in the morning 8AM and in evening 6PM as the people    might be going to their work at morning 8AM and returing from their work at the evening 6PM.
3. People prefered more rented bikes in the morning than the evening.
4. When the rainfall was less, people have booked more bikes except some few cases.
5. The Temperature, Hour & Humidity are the most important features that positively drive the total rented bikes count.
6.After performing the various models the lightGBM and Catboost found to be the best model that can be used for the Bike Sharing Demand Prediction since the performance metrics (mse,rmse) shows lower and (r2,adjusted_r2) shows a higher value for the lightGBM and Catboost models !
7. We can use either lightGBM or catboost model for the bike rental stations.



