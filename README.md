# Covid-19-Analysis

## Project Goal
The goal of this project is to investigate the impact of the pandemic on the housing prices in Polk, Florida. During the pandemic, the housing prices surged in the United States and presently it is still showing the sign of further uprise. This would suggested a lot of human centered implications, in terms of the economy, the society and political relationships. For houseowners, this could help them gain insights on their personal wealth and better manage their cost of livings. For investors, the relationship between the pandemic and house prices could be a significant factor when making investment decisions. Moreover, if there does exist a relationship between pandemic and house prices, it could say a lot of things about the economy as the house prices both reflect the ongoing economic/political policies, and signal potential future policies.

## Data
### Covid 19 data
In this project, we would be looking into the Covid-19 confirmed cases data, using the following datasets:
- The RAW_us_confirmed_cases.csv file from the Kaggle repository of John Hopkins University COVID-19 data: https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university.
- The CDC dataset of masking mandates by county:https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i. However, the CDC stopped collecting this policy information in September 2021.
- The New York Times mask compliance survey data: https://github.com/nytimes/covid-19-data/tree/master/mask-use. 

### House prices data
Since we would be investigating on the relationship between the house prices and Covid-19 cases, we would also be using the following data for the US house prices:
- Zillow Home Value Index (ZHVI): https://www.zillow.com/research/data/. The home type of “ZHVI all homes time series, smoothed, seasonally adjusted” is selected and geography location is specific to county. According to the description on the webpage, ZHVI is “a smoothed, seasonally adjusted measure of the typical home value and market changes across a given region and housing type”, and “reflects the typical value for homes in the 35th to 65th percentile range”.

This data contains the housing prices in the United States specific to the county level, including Polk, Florida. It also contains all other counties in the United States as well as their housing prices. The housing prices are a time series data taken as an average from all houses in the specific region at the end of each month. 

## Repo Info
This repository contains the following directories:
- `/data` contains all related data files
- `/img` contains all output images, including the visualization created for part 1
- `/src` contains all code and notebooks

## Linear Regression Results
| data | slope | y-intercept | R2 | std err | t value | p value |
| ---- | ----- | ----------- | -- | ------- | ------- | ------- |
| before covid | 33.91 | 168003.41 | 0.96 | 31.136 | 10.107 |  < 0.001 |
| after covid | 151.56 | 177446.25 | 0.94 | 31.388 | 13.965 | < 0.001 |


## Visualizations
The visualizations consist of two parts: first would be the autocorrelations and the cross correlations of the Polk infection rates and the US infection rate, and the second part consists of the relationship investigation of the Polk confirmed cases and Polk house prices.

## Polk Invection Rates
### Covid Confirmed cases in Polk
![Polk Covid](https://github.com/MatthewChau99/Covid-19-Analysis/blob/master/img/polk%20covid.png)

### Autocorrelation for Polk Infection Rate
![autocorr](https://github.com/MatthewChau99/Covid-19-Analysis/blob/master/img/auto_corr_polk.png)

### Cross Correlation between Polk daily increase and US daily increase
![cross corr Polk US](https://github.com/MatthewChau99/Covid-19-Analysis/blob/master/img/cross_corr_polk_us.png)


## Relationship with the House Prices
### House average Prices in Polk
![Polk House Prices](https://github.com/MatthewChau99/Covid-19-Analysis/blob/master/img/house%20avg%20prices.png)

### Linear regression of before and after covid for house prices
![Before Covid](https://github.com/MatthewChau99/Covid-19-Analysis/blob/master/img/lr_bef.png)
![After Covid](https://github.com/MatthewChau99/Covid-19-Analysis/blob/master/img/lr_aft.png)

### Interpolation of House Prices
![Interpoaltion of Polk House Prices](https://github.com/MatthewChau99/Covid-19-Analysis/blob/master/img/interpolation.png)

## Conclusion
- For lag from 1 to 25 days, there is strong evidence that some level of autocorrelation exists for Polk's Infection Rate, which impies that the daily increase of the past 1-25 days are highly correlated to the daily increase of the present day.
- The increase rate of housing prices in Polk does have a statistically significant difference between Covid and after Covid.
- The change in housing prices have a very strong correlation with the Covid Confirmed cases change in Polk, Florida, and the correlation decreases as the time lag decreases.

## References
(2022). Housing Data. Zillow. https://www.zillow.com/research/data/
