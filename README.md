|Problem Statement|:

Presently, there are a huge number of research papers and projects wherein stock price prediction is given importance to and an innumerable methodologies implemented in doing so. But, a stock exchange is not just about the stock prices over time. An index is formulated for a certain set of stocks which is much more meaningful as these indices are what decide the worth of the stocks that are being invested in. So, how can stock investment be made more significant and strategic? By predicting the index values over a long period of time, and doing so accurately, means that over that same period of time, the risk and returns associated with the predicted stock prices can be calculated which gives a much better understanding of the risk involved in investing in a particular stock over that period of time. Of course, doing so is not as easy as it sounds and just applying basic or advanced machine learning models will not suffice. Even with the implementation of deep learning models, the prediction accuracy and the margin of error associated with it is only achieved to a certain extent. Given this predicament, how can stock index be predicted such that the margin of error is minimized to a great extent and the predicted values can be relied upon by investors? 

|Research Question|:

1. "To what extent can the BSE(Bombay Stock Exchange) Index be predicted over a long period of time by implementing the prediction stacking method for various machine and deep learning models?"

2. "Can a custom formulated loss function minimize the margin of error for a deep learning model?"

|Solution developed|:

--> Features such as the simple moving averages, % change, Relative Strength Index (RSI), differences and ratios were engineered and selected based on correlations observed by plotting the correlation matrix using Seaborn.  

--> Evidently from the results observed during the course of this project, any chosen machine learning or deep learning model, individually, was able to minimize the margin of error only to a certain extent, which was not bad for a model but, given the volatility factor of a stock market, it just wasn't enough. 

--> Hence, to improve the results and minimize the error rate even further, a stacking methodology was used wherein, the predicted values obtained from different models individually, were stacked upon one another combining the predictive capabilities of each of these models. 

--> By stacking the best performing models, the results obtained provide evidence for the claim that stacking these models minimize the margin of error even further while improving the accuracy with which the values are predicted.

--> Machine learning models such as Linear Regression, Decision Tree Regressor, Random Forest Regressor, and Gradient Boosting Random Forest Regressor are implemented alongside deep learning models such as the Deep Neural Network, with and without dropout, and a Long-Short Term Memory network.

--> Metrics used to evaluate the models were R^2 score, Root Mean Squared Error(RMSE) and Mean Absolute Error(MAE).

--> Prior to the stacking method being implemented, individually, the LSTM network model achieved the least R^2 score of 0.9492, RMSE score of 0.0567 and an MAE score of 0.0451.

--> With the stacking methodology, different combinations of previously implemented models were developed, among which, the combination of the Random Forest Regressor, Deep Neural Network and the LSTM network (RF-DLSTM model stack) performed the best, with an R^2 score of 0.9660, RMSE score of 0.0503 and an MAE score of 0.0408. 

--> By plotting the predicted values produced by the above mentioned RF-DLSTM model stack against the true values over the chosen period of time (7 years from 2013 to 2020), predictions made were quite accurate and the projection of the predicted values is very close to the projection of the true values plotted. 

|Future Work|:

Beyond what has been achieved here in this research project, there is some scope for further work and improvement. As mentioned in the problem statement, it is important not only to predict the stock prices but also the stock index with the help of which the risk and returns for a praticular set of stocks can be determined. The research project here only focuses on the Index. Using a similar approach, by predicting the stock prices over the same period of time, will enable calculation of metrics such as the Sharpe ratio, average returns (daily, monthly and yearly) and predict return values of the chosen stocks. Automating the whole process further improves the prospect of this research project and such an improvement would definitely prove beneficial for an investor. 
