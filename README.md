# Time Series Analysis Project

Course project for Time Series Analysis. The goal is to model a real-world time series with two forecasting approaches, **interpret every step** (technically and in a business context), and compare the forecasts methodologically. It is not only about producing forecasts.

## Dataset

A dataset with timestamps and values that can be decomposed as:

**Yₜ = Tₜ + Sₜ + Rₜ** (trend + seasonality + residual)

The series should show a visible trend and seasonality, over several years of data.

## Approaches

### 1. ETS decomposition + ARIMA (understand and explore)

- Decompose Yₜ into trend (Tₜ), seasonality (Sₜ) and residual (Rₜ).
- Model the residual Rₜ with ARIMA:
  - stationarity checks (ADF / KPSS),
  - ACF / PACF analysis to choose the (p, d, q) orders,
  - residual diagnostics.
- Forecast by recombining the trend, the seasonality and the ARIMA forecast of Rₜ.
- Interpret each component, technically and in business terms.

### 2. Facebook Prophet (discover and compare)

- Understand how the method works: additive trend, seasonality, holidays, changepoints.
- Try different parameters (changepoint prior scale, seasonality mode, holidays, etc.) and interpret their effect.

## Forecast comparison

- Use the same train / test split for both approaches.
- Compare them with loss functions: MSE, RMSE, MAE, MAPE.
- Discuss when and why one approach performs better than the other.

## Report structure

The report is written in the Jupyter notebook [tsa-Rondal-Luka.ipynb](tsa-Rondal-Luka.ipynb):

1. Introduction
2. Data exploration
3. Approach 1: ETS decomposition + ARIMA
4. Approach 2: Prophet
5. Forecast comparison
6. Conclusion
7. AI-usage policy: the main prompts and how AI was used in the project

## Setup

Dependencies are managed with [uv](https://docs.astral.sh/uv/):

```bash
uv sync
```

Then open the notebook and select the `.venv` kernel.
