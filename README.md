# Correlation to Causation: A Causal Deep Learning Framework for Arctic Sea Ice Prediction

The paper **"Correlation to Causation: A Causal Deep Learning Framework for Arctic Sea Ice Prediction"** has been accepted in the _Causal AI for Robust Decision Making (CARD)_ Workshop in **Pervasive Computing and Communications (PerCom 2025)**. This research investigates the impact of causality-aware feature selection on the performance of deep learning models for Arctic Sea Ice Extent (SIE) prediction using daily and monthly datasets. Below, you will find details about the experiments conducted and links to the corresponding notebooks.

## Overview of the Experiments

We conducted experiments on two datasets: **Arctic Daily Data** and **Arctic Monthly Data**, using three deep learning model configurations for each dataset:

1. **DL_vanilla**: A hybrid GRU-LSTM model trained on all available features.
2. **DL_GC**: A hybrid GRU-LSTM model trained on causal features identified using the Granger Causality algorithm.
3. **DL_PCMCI+**: A hybrid GRU-LSTM model trained on causal features identified using the PCMCI+ algorithm.

Each model was evaluated based on standard metrics such as RMSE, MAE, and R² for lead times ranging from 1 to 6 months.

## Dataset Descriptions

### 1. Arctic Daily Data
- **Time Period**: 1979-2018
- **Variables**: 11 ocean-atmospheric variables, including surface pressure, wind velocity, specific humidity, and others.
- **Causal Features**:
  - **GC**: All features except sea surface temperature.
  - **PCMCI+**: Longwave radiation, snowfall, sea surface temperature, sea surface salinity, surface pressure, and sea ice extent.

### 2. Arctic Monthly Data
- **Time Period**: 1979-2021
- **Variables**: Same as daily data.
- **Causal Features**:
  - **GC**: All features except sea surface temperature.
  - **PCMCI+**: Longwave radiation, sea surface temperature, and sea ice extent.

## Experiment Notebooks

Each notebook includes data preprocessing, model training, evaluation, and visualization for a specific configuration. Click on a notebook link to explore the details.

### Arctic Daily Data

1. **DL_vanilla on Daily Data**  
   A traditional deep learning model using all available features.  
   [1-Month](./notebooks/DL_vanilla/Daily%20Data/ML%20based%20SIE%20Prediction%20(1-month).ipynb) | [2-Month](./notebooks/DL_vanilla/Daily%20Data/ML%20based%20SIE%20Prediction%20(2-months).ipynb) | [3-Month](./notebooks/DL_vanilla/Daily%20Data/ML%20based%20SIE%20Prediction%20(3-months).ipynb) | [4-Month](./notebooks/DL_vanilla/Daily%20Data/ML%20based%20SIE%20Prediction%20(4-months).ipynb) | [5-Month](./notebooks/DL_vanilla/Daily%20Data/ML%20based%20SIE%20Prediction%20(5-months).ipynb) | [6-Month](./notebooks/DL_vanilla/Daily%20Data/ML%20based%20SIE%20Prediction%20(6-months).ipynb)

2. **DL_GC on Daily Data**  
   A causality-driven model trained on features identified by the Granger Causality algorithm.  
   [1-Month](./notebooks/DL_GC/Daily%20Data/GC%20based%20SIE%20Prediction%20(1-month).ipynb) | [2-Month](./notebooks/DL_GC/Daily%20Data/GC%20based%20SIE%20Prediction%20(2-months).ipynb) | [3-Month](./notebooks/DL_GC/Daily%20Data/GC%20based%20SIE%20Prediction%20(3-months).ipynb) | [4-Month](./notebooks/DL_GC/Daily%20Data/GC%20based%20SIE%20Prediction%20(4-months).ipynb) | [5-Month](./notebooks/DL_GC/Daily%20Data/GC%20based%20SIE%20Prediction%20(5-months).ipynb) | [6-Month](./notebooks/DL_GC/Daily%20Data/GC%20based%20SIE%20Prediction%20(6-months).ipynb)

3. **DL_PCMCI+ on Daily Data**  
   A causality-driven model trained on features identified by the PCMCI+ algorithm.  
   [1-Month](./notebooks/DL_PCMCI+/Daily%20Data/PCMCI+%20based%20SIE%20Prediction%20(1-month).ipynb) | [2-Month](./notebooks/DL_PCMCI+/Daily%20Data/PCMCI+%20based%20SIE%20Prediction%20(2-months).ipynb) | [3-Month](./notebooks/DL_PCMCI+/Daily%20Data/PCMCI+%20based%20SIE%20Prediction%20(3-months).ipynb) | [4-Month](./notebooks/DL_PCMCI+/Daily%20Data/PCMCI+%20based%20SIE%20Prediction%20(4-months).ipynb) | [5-Month](./notebooks/DL_PCMCI+/Daily%20Data/PCMCI+%20based%20SIE%20Prediction%20(5-months).ipynb) | [6-Month](./notebooks/DL_PCMCI+/Daily%20Data/PCMCI+%20based%20SIE%20Prediction%20(6-months).ipynb)

### Arctic Monthly Data

1. **DL_vanilla on Monthly Data**  
   A traditional deep learning model using all available features.  
   [1-Month](./notebooks/DL_vanilla/Monthly%20Data/ML%20based%20SIE%20Prediction%20(1-month).ipynb) | [2-Month](./notebooks/DL_vanilla/Monthly%20Data/ML%20based%20SIE%20Prediction%20(2-months).ipynb) | [3-Month](./notebooks/DL_vanilla/Monthly%20Data/ML%20based%20SIE%20Prediction%20(3-months).ipynb) | [4-Month](./notebooks/DL_vanilla/Monthly%20Data/ML%20based%20SIE%20Prediction%20(4-months).ipynb) | [5-Month](./notebooks/DL_vanilla/Monthly%20Data/ML%20based%20SIE%20Prediction%20(5-months).ipynb) | [6-Month](./notebooks/DL_vanilla/Monthly%20Data/ML%20based%20SIE%20Prediction%20(6-months).ipynb)

## Results and Observations

- **Daily Data**: Models trained on causal features (GC and PCMCI+) generally outperformed the DL_vanilla model, especially for longer lead times.
- **Monthly Data**: Similar trends were observed, with causal models showing better predictive capability, particularly for PCMCI+ features derived from daily data.

## Future Directions

- Incorporating time lags for causal features into training to improve model performance.
- Exploring advanced architectures like Transformer models to enhance causal feature integration.

Feel free to navigate through the notebooks and explore how causality influences sea ice predictions.

