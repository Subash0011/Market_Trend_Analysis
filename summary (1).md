# Project Summary

## Dataset
- Source: Market Trend Analysis Dataset (Kaggle)
- Features: Prices, returns, volatility, SMA, RSI, MACD, Bollinger Bands
- Target: Closing price

## Models
- LSTM: 2 layers (64, 32 units), Adam optimizer with cosine decay
- Transformer: Encoder block (d_model=64, heads=4, ff_dim=128)
- Baselines: Prophet, SARIMA

## Metrics
- LSTM: {'RMSE': np.float64(2.198174203018401), 'MAE': 1.6379477350844491, 'MAPE': np.float64(7.309939558172954)}
- Transformer: {'RMSE': np.float64(3.4768695603875504), 'MAE': 2.7132559061657617, 'MAPE': np.float64(9.519325899863738)}
- Prophet: {'RMSE': np.float64(54.10355213322439), 'MAE': 44.637414906767376, 'MAPE': np.float64(412.8852246709412)}
- SARIMA: {'RMSE': np.float64(21.24692054946472), 'MAE': 18.13659009747799, 'MAPE': np.float64(141.0886482294201)}

## Interpretability
- SHAP shows top drivers: MACD_Value, High_Price, RSI_14, Low_Price, Volatility_Range
- Attention weights highlight volatility spikes and seasonal dependencies
