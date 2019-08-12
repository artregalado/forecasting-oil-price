# Forecasting the spot price of Mexican oil


Oil is one of the most important traded commodities in the world and a much needed resource for economic growth. Despite the undergoing energy transition, it remains a strong input in the world's primary energy mix. Notably, oil producing countries such as Mexico are affected, for better or worse, by its price.

Continuing with the example of Mexico, [oil revenues account for 18% of its government budget.](https://ciep.mx/ley-de-ingresos-de-la-federacion-2019/) When one fifth of the public budget comes from oil revenues, it is no exageration to say that the oil price could make or break the government's income. 

Consequently, one must-have ability of as energy analysts is forecasting oil price. **In this notebook I show how to forecast the price of the Mexican Crude Oil (MMA)**. I develop a highly simplified Vector Autorregressive Model (VAR) to showcase the fundamentals of undertaking time-series analysis **using Python** to forecast the MMA price.

If you've read about how to model time-series you will surely have heard about the ARIMA family of models. While they are useful in some situations I would argue that to forecast oil prices the VAR model is more suitable. These are the reasons:

+ VAR models allow for multivariate time-series analysis (ARIMA are univariate). This means that a variable can depend on its own lags or lags from other variables.
+ The literature has found that VAR results are often better than structural models.
+ It is flexible enough to model a mix of endogenous and exogenous variables. Therefore it can capture strucutral behaviours as well as external influences to the system.   

**In summary, the VAR model is flexible and generalizes easily**. For an introductory treatment of the model you can see Chris Brooks': *Introductory Econometrics for Finance*.

**Disclaimer:** I am providing a basic guide for the interested readers on how the basic issues need to be addressed. By no means this is an exhaustive treatment of how to do time-series forecasting. I don't argue it is the best or only way or that it is 100% correct. 
