# Energy Demand Forecasting with Deep Learning

This project implements a hybrid **CNN–LSTM–Transformer** model to forecast hourly electricity demand in New York City. The model leverages historical load data, weather information (temperature and humidity), and calendar features (holidays) to provide accurate short-term demand predictions.


## Features

* **Hybrid architecture** combining:

  * CNN layers for short-term temporal/spatial pattern extraction.
  * LSTM layers for sequential dependency modeling.
  * Transformer encoder for attention-based context learning.
* Sequence-based modeling using 24-hour lookback windows.
* Evaluation metrics including **MAE (Mean Absolute Error)**.
* Visualization of predictions vs. actuals, error analysis, and scatter comparisons.


## Dataset

* **Load Data**: Hourly demand data from NYISO.
* **Weather Data**: Hourly temperature and humidity for NYC, retrieved from the [Meteostat](https://dev.meteostat.net/) API.
* **Holiday Data**: US federal holidays via the `holidays` Python library.

All time series are aligned to the **America/New_York** timezone.


## Results

* The hybrid model achieves **test MAE ≈ 60 MW**, significantly improving over baseline LSTM and CNN-only models.
* Visualizations show strong alignment of predictions with actual demand, with errors primarily during peak transitions.

<img width="1796" height="498" alt="image" src="https://github.com/user-attachments/assets/db7a42e1-4ec3-4d13-aba8-b806b6baad29" />
