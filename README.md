# Time Series Analysis - A Yen for the Future


In this assignment, many time-series tools are used to predict future movements in the value of the Japanese yen versus the U.S. dollar.

## Time-Series Forecasting
Firstly, predictable behavior is achieved by loading the historical Dollar-Yen exchange rate futures data and apply time series analysis and modeling.
Next, these steps are carried out : 
( 1 ) Decomposition using a Hodrick-Prescott Filter (Decompose the Settle price into trend and noise).
( 2 ) Forecasting Returns using an ARMA Model.
( 3 ) Forecasting the Settle Price using an ARIMA Model.
( 4 ) Forecasting Volatility with GARCH


## Linear Regression Forecasting
Secondly, Scikit-Learn linear regression model to predict Yen futures ("settle") returns with lagged Yen futures returns and categorical calendar seasonal effects (e.g., day-of-week or week-of-year seasonal effects) are built in this aspect.
Next, these steps are carried out : 
( 1 ) Data Preparation (Creating Returns and Lagged Returns and splitting the data into training and testing data)
( 2 ) Fitting a Linear Regression Model.
( 3 ) Making predictions using the testing data.
( 4 ) Out-of-sample performance.
( 5 ) In-sample performance.

Based on the results of the time series analysis and modeling, the ARMA (autoregressive moving average) model does not appear to be a good fit because the p-values are higher (>0.05). Additionally, the ARIMA (autoregressive integrated moving average) model that predicts future Yen prices states that p-values are realtively high.  As such, the ARIMA model does not appear to be a good fit for this dataset.  Volatility of the Yen is forecasted using GARCH (generalized autoregressive conditional heteroskedasticity) model.  The p values of the GARCH model seems low which makes it a good fit to predict the volatility of the Japanese Yen.

Drawing upon this time series analysis, I would not buy the Japanese Yen. Reason being, it's too volatile from my perspectives, and the GARCH model suggests that volatility will likely to increase over time. 
