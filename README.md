# Stock_Market_Project

### Prepared by: 

|Name     |  Github   | 
|---------|-----------------|
|[Abzal Seitkaziyev](https://github.com/xs-abzal)


### Data Source
The data for this project was obtained from Yahoo Finance using [yfinace](https://pypi.org/project/yfinance/). 

### Jupyter notebooks
*  [Get data](https://github.com/xs-abzal/Stock_Market_Project/blob/master/notebooks/0_get_data.ipynb)
*  [S&P500](https://github.com/xs-abzal/Stock_Market_Project/blob/master/notebooks/1_portfolio%20of%20few%20stocks%20and%20snp500.ipynb)
*  [Stocks](https://github.com/xs-abzal/Stock_Market_Project/blob/master/notebooks/2_portfolio%20of%20409%20stocks.ipynb)


### Project Presentation
[Google Slides]()


### Problem Summary
For this project I explored ML models along with trading strategies which can output more profit than long term investment. Particulary, I applied classification model to predict when to enter positions in swing trading and used trailing stop loss to exit positions.

### Metrics
For this project I didnt use precision or f1 score, but used roc_auc as a main metric. It is due to the nature of the target, model picks up some local minima with order of less than 10 days(I used true local minima with 10 days to each side). With correct implementation of stop-loss, we can avoid real false positives. However, I chose threshold for probability of the model(e.g.=0.8) with higher f1 and precision score.

### Key Takeaways
Choosing stocks in bulk without prior screening still profitable, but cannot beat the long term investment return.However, individual models were able to beat long term investment. Model works better with balanced trading strategy.

S&P500 ROI with model = 1.5 vs long term investrment ROI =1.22

![S&P500](https://github.com/xs-abzal/Stock_Market_Project/blob/master/graph/snp.png)

### Next Steps
Improve Strategy by select Initially High Potential Portfolio and optimizing exit strategy for each stock.
Explore which combination of strategy and model beats popular trading strategies.
Improve Modelling by using Multiple Specialized models with most important features.

