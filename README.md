# Prediction of Fatal Shootings using Time Series and Mixed Effect Model

This repository contains the final project for DATA2020 at Brown University (Spring 2022), supervised by Prof. Alice Paul. Our team explored the prediction of fatal police shootings in the United States using time series modeling and mixed-effect modeling approaches.

## 📊 Project Overview

After the underreporting of police fatal shootings came to light following the 2014 Ferguson incident, we aimed to develop data-driven methods to:
- Forecast the number of monthly fatal shootings in upcoming quarters
- Predict fatal shooting counts by demographic groups (race)
- Investigate correlations between income, region, and shooting counts

## 🛠️ Methods Used

### Data Sources
- [Washington Post Fatal Police Shootings Database](https://github.com/washingtonpost/data-police-shootings)
- [U.S. State Demographics by Race](https://worldpopulationreview.com/states/states-by-race)
- [BEA Regional Income Statistics](https://apps.bea.gov/regional/downloadzip.cfm)

### Data Processing
- Cleaned missing values in location and demographic fields
- Created categorical bins for age and armed status
- Merged external datasets (income and race distribution)

### Models
- **ARIMA Time Series Models** for forecasting counts by race
- **Negative Binomial Mixed Effect Model** to model count data by race and region

## 📈 Key Findings

- Fatal shooting counts vary significantly across regions and racial groups.
- Income is not a statistically significant predictor in isolation.
- Race is a significant predictor, and models accounting for region as a random effect perform better.

## 📁 Folder Structure

```
├── data/              # Raw and cleaned datasets
├── scripts/           # R scripts for data cleaning, EDA, modeling
├── report/            # Presentation and write-up files
└── README.md
```

## 📌 Results Summary

- Time series forecasts from 2015–2020 show stable or slightly increasing trends for some racial groups.
- Mixed-effect models achieved:
  - Marginal R²: 0.794
  - Conditional R²: 0.877
  - MAE on predictions: ~5

## 📅 Future Work

- Expand analysis with more recent data post-2020
- Improve granularity of income data (e.g., by race within state)
- Incorporate additional socio-economic indicators (e.g., unemployment)

## 👥 Authors

- **Hanjun Wei** – Mixed Effects Model, Visualization, External Data Cleaning  
- **Keying Gong** – ARIMA Modeling, Map Visualization, Model Tuning  
- **Yurui Zhang** – Data Cleaning, EDA, External Data Research

## 📚 Citations

1. [Washington Post Police Shootings Database](https://github.com/washingtonpost/data-police-shootings)  
2. [US States by Race - World Population Review](https://worldpopulationreview.com/states/states-by-race)  
3. [BEA Personal Income Data](https://apps.bea.gov/regional/downloadzip.cfm)
