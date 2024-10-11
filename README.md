# Statistical Analysis and Forecasting of Solar Energy (Intra-State)

## Project Overview

This project presents a comprehensive **statistical analysis** and **time series forecasting** framework for solar energy generation based on solar irradiance and atmospheric data. The objective is to identify critical patterns and trends and apply advanced forecasting techniques to accurately predict solar energy generation, supporting informed decision-making for intra-state solar energy management.

## Key Objectives
1. **Exploratory Data Analysis (EDA)**: Conducted in-depth analysis to uncover relationships between solar irradiance and atmospheric variables.
2. **Factor Analysis**: Performed statistical tests to identify underlying factors influencing solar energy production.
3. **Time Series Decomposition**: Separated solar irradiance data into trend, seasonal, and residual components to extract meaningful insights.
4. **Time Series Forecasting**: Developed and compared multiple statistical and deep learning models, including AR, MA, ARIMA, SARIMA, Facebook Prophet, LSTM, and GRU, for accurate forecasting of solar energy trends.

## Detailed Workflow

### 1. Exploratory Data Analysis (EDA)
- **Correlation Heatmap**: Generated visualizations to explore relationships between features such as `Global Horizontal Irradiance (GHI)`, `Direct Normal Irradiance (DNI)`, `Temperature`, and `Solar Zenith Angle`.
- Key trends and relationships were identified to inform the selection of predictive features for model development.

### 2. Factor Analysis
- **Bartlett’s Test of Sphericity** and **Kaiser-Meyer-Olkin (KMO) Test** were conducted to evaluate data suitability for factor analysis.
- Extracted latent factors provided insight into the primary drivers of solar energy generation, including atmospheric variables and irradiance patterns.

### 3. Time Series Decomposition
- Decomposed the daily **GHI** time series data into:
  - **Trend**: Long-term upward/downward movement in solar irradiance data.
  - **Seasonal**: Repeating short-term patterns driven by daily and yearly solar cycles.
  - **Residual**: Noise and irregular variations.
  
  This decomposition was critical for understanding both the long-term and cyclical behaviors of solar energy generation.

### 4. Time Series Forecasting Models

- **Autoregressive (AR), Moving Average (MA), ARIMA, and SARIMA**: 
  - Applied statistical models to capture the autoregressive and moving average components of solar irradiance data. Model evaluation was based on 
  **Akaike Information Criterion (AIC)** and **Mean Absolute error(MAE)**, and these metrics were used to fetch the best values of the parameters 
   for a particular model. 
   The SARIMA model, which accounts for seasonality, was particularly useful for capturing daily and yearly cyclic patterns. 
  
- **Facebook Prophet**: 
  - Employed Facebook Prophet for time series forecasting due to its robustness in handling missing data and its ability to model trends and 
    seasonality explicitly. The model’s additive seasonality was ideal for capturing both daily and yearly patterns.
  
- **LSTM (Long Short-Term Memory) and GRU (Gated Recurrent Unit)**:
  - Implemented deep learning models designed to capture long-term dependencies and sequential relationships in the time series data. Both LSTM and GRU were trained on the temporal features of solar irradiance to predict future values. Model configuration involved using time-step lags and multiple layers to improve the model’s ability to capture complex patterns in the time series.

### 5. Model Validation and Performance
- Forecast accuracy was evaluated using metrics such as **Mean Absolute Error (MAE)** and **Mean Absolute Percentage Error (MAPE)**.
- The best-performing models were selected based on their predictive performance over both short-term and long-term horizons.

## Technologies and Libraries Used
- **Python**: Primary language for data analysis and model development.
- **Pandas, Seaborn, Matplotlib**: Employed for data wrangling, visualization, and exploratory analysis.
- **Statsmodels**: Used for statistical time series modeling (ARIMA, SARIMA).
- **Scikit-learn**: Applied for data preprocessing and hyperparameter tuning.
- **TensorFlow/Keras**: Utilized for developing deep learning models (LSTM, GRU).
- **Facebook Prophet**: Implemented for forecasting with flexible trend and seasonality components.

## Conclusion
This project provides a robust framework for understanding and forecasting solar energy generation using a combination of traditional statistical models and advanced deep learning techniques. The insights gained from the time series analysis and the accurate forecasts can be leveraged for optimizing intra-state solar energy generation strategies. Future work could explore real-time integration of weather data for dynamic forecasting and experiment with hybrid models to enhance predictive performance.

