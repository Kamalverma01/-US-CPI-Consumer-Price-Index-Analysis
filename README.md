# US Consumer Price Index (CPI) Time Series Forecasting

## Objective

This project aims to develop an accurate time series forecasting model to predict the future values of the US Consumer Price Index (CPI). Specifically, the goals are to:

1. Understand what CPI is and how it is related to inflation of an area, city, state, country, or globally.
2. Analyze historical CPI data to identify patterns and trends.
3. Preprocess the data for accuracy.
4. Evaluate and select the best forecasting model.
5. Provide reliable predictions for future inflation trends.

The goal is to provide valuable insights into future inflation trends to aid in economic decision-making.

---

## 1. Understanding CPI and Its Relation to Inflation

### What is CPI?

The Consumer Price Index (CPI) measures the average change in prices paid by consumers for goods and services over time, reflecting the cost of living.

### Relation to Inflation:

- **Inflation Rate:** Calculated using CPI to indicate how fast prices are rising.
- **Regional Analysis:** CPI can be analyzed for cities, states, or countries to reflect local economic conditions.
- **Global Perspective:** Comparing CPI across countries provides insights into global economic stability.

### Applications of CPI:

- **Adjusting Income:** Governments use CPI to adjust wages and benefits.
- **Policy Decisions:** Central banks use CPI for monetary policy.
- **Economic Analysis:** Economists gauge economic health using CPI.

In summary, CPI helps understand and manage inflation, informing policy decisions and economic strategies.

---

## 2. Analysis of Historical US CPI Data (1910-2020)

We analyzed the historical data of the United States Consumer Price Index (CPI) from 1910 to 2020 to identify patterns and trends.

### Period of 1910 to 1940

During this period, CPI showed minimal change, attributed to economic policies and market conditions, including the impact of the Great Depression.

### Post-1940 Trend

From 1940 onwards, CPI increased significantly, reflecting economic growth, post-war reconstruction, and inflationary pressures due to increased consumer demand.

### Seasonality

Distinct seasonal trends were identified, influenced by factors like weather, holidays, and agricultural cycles.

---

## 3. Data Preprocessing for Accuracy

In the preprocessing phase, we ensured the data's accuracy by:

- **Missing Values:** Conducted analysis to detect any missing values, ensuring the integrity of the data.
- **Data Resampling:** The dataset was already recorded at monthly intervals, so no resampling was required.

Additionally, we performed stationarity tests such as ADF (Augmented Dickey-Fuller) and KPSS (Kwiatkowski-Phillips-Schmidt-Shin) tests. Both tests confirmed that the series was non-stationary.

---

## 4. Evaluation and Selection of the Best Forecasting Model

### Models Evaluated:

1. **SARIMA (Seasonal AutoRegressive Integrated Moving Average)**
   - We analyzed the ACF and PACF plots to determine the values of p, d, q, P, D, Q, and S.
   - Used evaluation metrics like RMSE and MSE to assess model performance.

2. **AutoARIMA (Automatic ARIMA)**
   - AutoARIMA automatically identifies the best ARIMA model by testing different parameter combinations and selecting the optimal set based on chosen criteria.

3. **Holt-Winters Exponential Smoothing**
   - A time series forecasting method that accounts for trend and seasonality, focusing on recent historical data to make immediate or near-future predictions.

---

## 5. Result

After evaluating the models using performance metrics such as Mean Squared Error (MSE) and Root Mean Squared Error (RMSE), and analyzing the prediction plots, we concluded the following:

- **Holt-Winters Exponential Smoothing** provided the most accurate results, with the lowest MSE and RMSE among the models.
- This model was chosen to forecast the US CPI for the next 12 months, ensuring reliable and precise predictions for economic analysis.

---

## Future Work

- **Model Refinement:** Further refinement of the forecasting models by incorporating more advanced techniques such as deep learning for time series forecasting.
- **Additional Features:** Integrating external economic indicators (e.g., unemployment rates, consumer sentiment) to improve model accuracy.

---

## Requirements

To run the code and replicate the analysis, ensure you have the following libraries installed:

- Python 3.x
- pandas
- numpy
- statsmodels
- matplotlib
- seaborn
- pmdarima (for AutoARIMA)
- jupyter notebook (optional, for interactive development)

To install the required libraries, run:

```bash
pip install pandas numpy statsmodels matplotlib seaborn pmdarima
