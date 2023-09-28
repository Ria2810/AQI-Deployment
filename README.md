# Air Quality Index (AQI) Prediction
This GitHub repository contains a project for predicting the Air Quality Index (AQI) for Bangalore. The project involves data scraping, data preprocessing, exploratory data analysis, model training, and deployment of a web application for AQI prediction. This README provides detailed information about the project and its components.

## Table of Contents
1. Data Scraping
2. Data Sources
3. Data Description
4. Data Preprocessing
5. Exploratory Data Analysis
6. Model Training
7. Deployment

### <ins>Data Scraping</ins>
The project began with web scraping using the Beautiful Soup library to collect weather-related data for Bangalore. This data was extracted from tutiempo.net and covered the years 2013 to 2017 for each month.

### <ins>Data Sources</ins>
- The primary data sources for this project are as follows:

- Weather Data: Weather data for Bangalore was scraped from tutiempo.net.
Air Quality Data: Hourly AQI values for Bangalore were obtained from the openweatherapi.
### <ins>Data Description</ins>
The combined dataset consists of the following features for each day:

- T: Average temperature (°C)
- TM: Maximum temperature (°C)
- Tm: Minimum temperature (°C)
- SLP: Atmospheric pressure at sea level (hPa)
- h: Average relative humidity (%)
- PP: Total precipitation of rain and/or melted snow (mm)
- V.V.: Average visibility (Km)
- V: Average wind speed (Km/h)
- V.M.: Maximum sustained wind speed (Km/h)
- V.G.: Maximum wind gust speed (Km/h)
- R.A.: Indicates whether there was rain or drizzle (In the monthly average, total days that it rained)
- S.N.: Snow indicator (In the monthly average, total days that it snowed)
- T.S: Indicates if there was a storm (In the monthly average, total days with a storm)
- F.G.: Indicates if there was fog (In the monthly average, total days with fog)
  
### <ins>Data Preprocessing</ins>
- The data preprocessing step involved:
- Dropping columns with null values.
- Eliminating missing values from the dataset.
  
### <ins>Exploratory Data Analysis</ins>
Exploratory Data Analysis (EDA) was performed to understand the data better. Key steps included:

- Calculating correlations between variables and visualizing them using a heatmap.
- Determining feature importance using the ExtraTreesRegressor() method to identify the most significant variables for AQI prediction.
  
### <ins>Model Training</ins>
Several machine learning algorithms were utilized for AQI prediction. These include:

- Linear Regression
- Random Forest
- Decision Tree
- XGBoost
The models were evaluated using metrics such as R-squared, Mean Absolute Error (MAE), and Mean Squared Error (MSE). The model with the best performance was selected, and a serialized pickle file was created to save the trained model.

### <ins>Deployment</ins>
A web application was developed using Flask to deploy the trained model. The web application accepts real data for the year 2018 as input and predicts the AQI value for all 365 days.
