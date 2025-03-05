# Bike Sharing Demand Prediction
>  This project aims to model the demand for shared bikes based on various independent variables.  The model will help management understand how demand fluctuates with different features, enabling them to adjust business strategies to meet demand and customer expectations.  It will also provide insights into demand dynamics in new markets.



## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- What is the background of the project?<br>
	- A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.
- What is the business probem that your project is trying to solve?<br>
	- You are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 
- What is the dataset that is being used?
    - The dataset 'day.csv' have the following fields:
        - instant: record index
        - dteday : date
	    - season : season (1:spring, 2:summer, 3:fall, 4:winter)
	    - yr : year (0: 2018, 1:2019)
	    - mnth : month ( 1 to 12)
	    - holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	    - weekday : day of the week
	    - workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	    - weathersit : 
		    1. Clear, Few clouds, Partly cloudy, Partly cloudy
		    2. Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		    3. Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		    4. Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	    - temp : temperature in Celsius
	    - atemp: feeling temperature in Celsius
	    - hum: humidity
	    - windspeed: wind speed
	    - casual: count of casual users
	    - registered: count of registered users
	    - cnt: count of total rental bikes including both casual and registered
- Project Steps

1. **Data Loading and Exploration:**
    - Load the bike-sharing dataset (`day.csv`).
    - Explore data types, check for missing values, and perform descriptive statistics.
    - Visualize data using various plots (bar plots, pair plots, heatmaps, box plots) to understand relationships between variables, identify outliers and multicollinearity.
    - Reverse label encoding of categorical variables for EDA.

2. **Data Preprocessing:**
    - Drop irrelevant columns (`instant`, `casual`, `registered`, `atemp`).
    - Handle outliers.
    - Address multicollinearity by removing highly correlated features ('yr', 'mnth', 'hum', 'season') using VIF and correlation analysis.
    - Further feature engineering if necessary.


3. **Model Building:**
    - Split data into training and testing sets.
    - Train a linear regression model.
    - Make predictions on the test set.

4. **Model Evaluation:**
    - Evaluate model performance using R-squared and visualization of actual vs. predicted values.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- The project successfully builds a linear regression model to predict bike-sharing demand. The model performance is evaluated using R-squared metric and a visual comparison of predictions against actual values.  Data exploration and preprocessing steps, including handling outliers and multicollinearity, were critical in achieving reasonable model accuracy of ~ 71 %.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- pandas==1.5.3
- numpy==1.23.5
- matplotlib==3.7.1
- seaborn==0.12.2
- scikit-learn==1.2.2
- statsmodels==0.13.5

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
I would like to thank Upgrad for giving me this opportunity to work on this project.


## Contact
Created by [Anirudha Kumar Sahu](https://github.com/anirudhasahu92) - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->