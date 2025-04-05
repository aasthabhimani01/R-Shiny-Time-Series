# R-Shiny-Time-Series
A comprehensive Shiny dashboard for time series exploration, stationarity checks, model fitting (ARIMA, ARCH, GARCH), forecasting, diagnostics and visualization. Includes ACF/PACF plots, model suggestions and user specified forecast horizons. 

Time Series Analysis Dashboard in R Shiny 
========================================= 
Overview 
-------- 
An interactive and educational Shiny web application for time series analysis. It allows graphical exploration, stationarity checks, decomposition, model fitting (ARIMA, ARCH, GARCH), diagnostics, and forecasting. 
Features 
-------- 
- Upload and analyze CSV time series data. 
- EDA: Handle missing/duplicate values. 
- ACF/PACF for original & stationary data. 
- Auto stationarity via transformations. 
- ADF Test for stationarity. 
- Model suggestions: AR, MA, ARIMA, ARCH, GARCH. 
- Residual diagnostics. 
- Forecasting with user-defined horizon. 
- Downloadable results. 
Getting Started 
--------------- 
Install dependencies: 
install.packages(c("shiny", "ggplot2", "forecast", "tseries", "rugarch", "zoo", "FinTS", "TTR", "dplyr"))
Run app: 
shiny::runApp("grp1_team_task") 
Usage Instructions 
------------------ 
1. Upload CSV file. 
2. Select time series column. 
3. Explore via EDA tab. 
4. View ACF/PACF (original & stationary). 5. App applies transformations as needed. 6. Choose model or use auto suggestion. 7. Forecast with selected horizon. 
8. Download outputs. 
Interpretation Guide 
-------------------- 
EDA: 
- Missing -> Imputed (mean) 
- Duplicates -> Removed 
- Trend/Seasonality shown 
Stationarity: 
- ADF test: p < 0.05 -> stationary 
- Differencing/log transform applied if non-stationary ACF/PACF:
- ACF/PACF cutoff patterns help identify model orders 
Model Selection: 
- auto.arima() suggests best ARIMA(p,d,q) 
- ARCH/GARCH used if volatility clustering present 
Diagnostics: 
- White noise residuals expected 
- Ljung-Box test: p > 0.05 -> no autocorrelation 
Forecasting: 
- User sets forecast horizon 
- Outputs include confidence intervals 
Dependencies 
------------ 
- shiny, ggplot2, forecast, tseries, rugarch, zoo, FinTS, TTR, dplyr 
Credits 
------- 
Developed by a 5-member academic team for an advanced time series project.
