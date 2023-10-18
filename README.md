# Analysing monthly number of sunspots
A time series analysis project on the R dataset sunspots.month. Exploring the different components of the time series data and choosing an appropriate model to forecast the future.
## Sunspots
What are they?
Sunspots are dark regions on the surface of the Sun. They are caused by twisting, chaotic magnetic fields from within the Sun's convective zone. These powerful magnetic disturbances produce active regions on the Sun, which can often create: 
1. Solar flares
2. Coronal mass ejections (CMEs)
## Procedure: 
Broke the work into few steps.
### Exploratory Data Analysis
First plotting the data to get a visual representation of it and trying to pick up something through the visualization about the data.
Some very interesting insights from the plots are:
1. Irregular Trend
2. Strong Cyclical Pattern (of 9-10 years of periodicity)
### Modelling and Deseasonalization
Then decomposed the data and then deseasonalized it. As the dataset is a big one, so splitting the data into a test and a training set made sense, which would come in handy for testing the model forecasting accuracy.
Then plotting the acf and pacf plots which showed that we need to implement ARIMA as there were points above the significant level for both of them.
Also used the exponential smoothing technique.
### Forecasting and model choosing
Then forecasted for the data and then tried to see the accuracy with the test dataset (used the forecast mean for accuracy) and plotted the residuals, it clearly shows that the cyclical component of the time series has creeped into the residuals.
Comparing the AIC and also the test error rate we conclude that the ARIMA(2,1,2) is the better model for this data than the exponential smoothing data.
