AirQuality-Prediction
Webapp to predict the Air Quality Index of a region given climate conditions.


1. Data Collection: (execute main-aqi.py)
For this step, I have written a web scrapper that scraps en.tutiempo.net for climate data from 2013 to 2015 and creates a HTML file for each month.

2. Data Preprocessing: (execute main-aqi.py)
This data contained hourly measurements of AQI.
This was converted into a dictionary format where the dictionary key is the year and values are the daily AQI values.
Next, the data in step 1 was combined with data of this step to create a new CSV file.

3. Data Cleaning: (execute main-aqi.py)
The CSV file created in step 2 was cleaned to remove null values and improper data. A new resultant CSV file was created.
Feature Engineering and Model Creation: (execute individual jupyter notebooks)
Tried various algorithms, like Linear Regression, Lasso and Ridge Regression, Decision Tree Regressor, KNN Regressor, Random Forest Regressor, XGBoost Regressor.
Random Forest and XGBoost gave best performance. Finally, used XGBoost to perform predictions.

4. Model Deployment: (execute flask-app in project root, npm build in aqi-frontend folder and hit http://localhost:5000/aqi-frontend)
Used React.js frontend to make API calls to Flask REST API backend.
Finally deployed on Heroku platform.
You can enter various climate details or select one of the popular cities. Finally, click submit button and get your results for Air Quality Index.
