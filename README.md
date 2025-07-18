# Ride-Hailing Fare Prediction

This project was developed as part of a hackathon for the Data Analytics course at PES University.  This project aims to analyze and forecast average fares for a ride-hailing service in Quahog City using advanced time series and statistical modeling. The analysis covers multiple vehicle types (car, bike, auto) and leverages external factors like weather, traffic, and special events.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Tasks & Methodology](#tasks--methodology)
  - [1. Data Exploration and Preparation](#1-data-exploration-and-preparation)
  - [2. Time Series Characterization](#2-time-series-characterization)
  - [3. Advanced Forecasting and Feature Engineering](#3-advanced-forecasting-and-feature-engineering)
- [Key Results](#key-results)
- [How to Run](#how-to-run)
- [Dependencies](#dependencies)
- [References](#references)

---

## Overview

This repository contains a complete workflow for fare prediction in a ride-hailing context. It covers:
- Exploratory Data Analysis (EDA)
- Time series analysis and stationarity checks
- Forecasting using Holt, Holt-Winters, and SARIMAX models
- Feature engineering and variable importance analysis

## Dataset

The data consists of historical ride records, including:
- Timestamp
- Rides completed
- Driver availability
- Surge multiplier
- Vehicle type (car, bike, auto)
- Weather conditions
- Traffic index
- Special event indicator

## Tasks & Methodology

### 1. Data Exploration and Preparation
- Inspected data distributions and feature correlations.
- Visualized trends in average fares per vehicle type.
- Performed ANOVA to test the effect of weather on fares.
- Encoded categorical variables for modeling.

### 2. Time Series Characterization
- Grouped and visualized average fares by vehicle type over time.
- Checked stationarity with the Augmented Dickey-Fuller (ADF) test.
- Applied Holt’s linear and Holt-Winters seasonal models for forecasting.

### 3. Advanced Forecasting and Feature Engineering
- Differenced non-stationary series and selected ARIMA/SARIMAX parameters using ACF/PACF.
- Engineered features: weather dummies, surge multiplier, driver availability, traffic index, special events.
- Evaluated feature importance based on model coefficients and error metrics (MSE, MAE).

## Key Results

- Strong negative correlation between average fare and rides completed.
- Weather alone is not a significant predictor, but surge multipliers during stormy/rainy conditions raise fares.
- SARIMAX with engineered features achieves low MSE and MAE in fare forecasting for cars and bikes.


## Dependencies

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- statsmodels
- scikit-learn

(See notebook for exact package versions.)
