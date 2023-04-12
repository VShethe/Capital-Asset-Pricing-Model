
# Capital Asset Pricing Model





## Table of Content


1. NSE - Capital Asset Pricing Model
 - Calculating Beta of Stocks.ipynb
 - Capital Asset Pricing Model - INFY,NIFTY.ipynb

2. USA Stocks - Capital Asset Pricing Model
 - Capital Asset Pricing Model.ipynb

## Project Description

1. **Capital Asset Pricing Model**
The Capital Asset Pricing Model (CAPM) is a financial model that uses linear regression to estimate the expected return on an asset given its risk and the risk-free rate of return.

```bash
Calculating beta of a stock:

Stock_beta = cov_with_market/market_var

```

![image](https://user-images.githubusercontent.com/128286364/231127503-0abdfe4b-8003-4485-a29d-3f19ebdb838d.png)


```bash
Calculating Expected Return of Stock (CAPM):

STOCK_ER = risk_free_rate + beta * market_risk_premium

market_risk_premium:
url: <https://pages.stern.nyu.edu/~adamodar/New_Home_Page/datafile/ctryprem.html>
```

```bash
Sharpe Ratio Formula:

Sharpe = (Stock_ER - risk_free_rate)/(sec_returns['Stock'].std())
```
## Installation

To install iexfinance:

url: <https://pypi.org/project/iexfinance/>

url: <https://iexcloud.io/>
```bash
pip install iexfinance
```
To install NSEpy:

url: <https://nsepy.xyz/>
```bash
pip install nsepy
```

## Deployment

To deploy this project run

```bash
  import numpy as np
  import pandas as pd
  import matplotlib.pyplot as plt
  from datetime import datetime
  from pandas_datareader import data as wb
```

```bash
  from iexfinance.stocks import Stock, get_historical_data

  start = datetime(2018, 1, 1)
  end = datetime(2023, 3, 23)

  api_key = 'API_KEY'
```

Creating a portfolio:
```bash
tickers = ['Stocks']
mydata = pd.DataFrame()
for t in tickers:
    mydata[t] = get_historical_data(t, start, end, output_format = 'pandas', token=api_key)['close']
```
