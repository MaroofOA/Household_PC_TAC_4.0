# Individual Household Electric Power Consumption

## Project Overview
This project involves analyzing and forecasting electric power consumption data from a single household in Sceaux, France, over a period of nearly four years. The data, sampled at a one-minute frequency, offers insights into various electrical quantities and sub-metering values recorded between December 2006 and November 2010. The goal of this project is to utilize time series forecasting techniques (both univariate and multivariate) to predict future power consumption trends and provide actionable insights.

## Dataset Description
The dataset consists of 2,075,259 measurements spanning 47 months. It includes the following features:

- **Global_active_power**: Total active power consumed by the household (in kilowatts).
- **Global_reactive_power**: Total reactive power consumed (in kilowatts).
- **Voltage**: Voltage levels (in volts).
- **Global_intensity**: Total current intensity (in amperes).
- **Sub_metering_1**: Active energy consumed by the kitchen (in watt-hours).
- **Sub_metering_2**: Active energy consumed by the laundry room (in watt-hours).
- **Sub_metering_3**: Active energy consumed by electric heating and air-conditioning (in watt-hours).

### Important Notes:
1. The variable `(global_active_power * 1000 / 60 - sub_metering_1 - sub_metering_2 - sub_metering_3)` represents the energy consumed by other household equipment that is not captured by the three sub-meterings.
2. The dataset contains some missing values (about 1.25% of the rows). While all calendar timestamps are present, certain measurement values are missing and represented by empty values between consecutive semicolons (e.g., missing values on April 28, 2007).

## Methods
The project applies both **univariate** and **multivariate** time series forecasting techniques to predict future power consumption. The methodologies include:

- **Univariate forecasting**: Predicting future values based solely on the historical values of a single variable (e.g., global active power).
- **Multivariate forecasting**: Incorporating multiple variables (e.g., global active power, voltage, sub-metering values) to improve the accuracy of predictions.

### Models Used:
- **Autoregressive Integrated Moving Average (ARIMA)** for univariate forecasting.

## Objectives
- To predict future household power consumption patterns using historical data.
- To explore the relationship between different power consumption variables and sub-metering data.
- To handle and impute missing data effectively for accurate predictions.

## Data Preprocessing
- **Missing Value Handling**: Imputed missing values using interpolation and forward-filling techniques.
- **Feature Engineering**: Generated new features such as hourly and daily averages to improve model performance.

## Results
The time series forecasting models provided meaningful insights into the household’s future power consumption trends. The multivariate models, were able to capture more complex relationships in the data compared to univariate models.

## Conclusion
This project demonstrates the application of time series forecasting in predicting household power consumption. The models can be extended to more complex use cases, such as demand-side energy management or smart grid applications.
