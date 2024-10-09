# AI and ML-Based Battery Management System for Electric Vehicles

## Problem Statement
The primary challenge in electric vehicle (EV) battery management lies in optimizing battery performance while extending its lifespan and ensuring safety. Traditional methods for estimating the State of Charge (SoC) and State of Health (SoH) often lack accuracy, leading to suboptimal battery usage and reduced lifespan. Additionally, predicting battery degradation patterns remains a complex task due to the various factors influencing battery health.

**Challenges to Address**:
1. Accurate estimation of SoC and SoH.
2. Prediction of battery degradation patterns.
3. Effective thermal management to prevent overheating and ensure optimal performance.

## Objective
The objective of this project is to develop an AI and Machine Learning-based battery management system for EVs that addresses the challenges mentioned above. The system aims to:
1. Enhance the accuracy of SoC and SoH estimation using advanced AI and ML algorithms.
2. Predict battery degradation patterns to optimize battery life and performance.
3. Implement effective thermal management strategies to maintain optimal battery temperature.

## Project Structure
The project contains the following directories:
- **datasets/**: Contains the battery datasets used in the project.
- **soc/**: Contains models and scripts related to SoC estimation (CNN, LSTM, DNN, XGBoost).
- **soh/**: Contains models and scripts related to SoH estimation.
- **pics/**: Stores images and plots generated during model training and evaluation.
- **.ipynb_checkpoints/**: Jupyter Notebook checkpoints.
  
## Models Used
Several machine learning and deep learning models were used for the estimation of SoC and SoH:
- **CNN (Convolutional Neural Network)**: Used for pattern recognition in time series and sensor data.
- **LSTM (Long Short-Term Memory)**: Applied for time series prediction to capture long-term dependencies.
- **DNN (Deep Neural Network)**: For accurate non-linear approximations.
- **XGBoost**: Gradient boosting algorithm optimized for regression tasks.

## Results

### A. SoC Estimation
The four variants developed for estimating the State of Charge (SoC) were DNN, CNN, LSTM, and XGBoost. The models were evaluated based on key metrics including Mean Absolute Error (MAE), Mean Square Error (MSE), Root Mean Square Error (RMSE), R-squared (R²), and Explained Variance.

| Model   | MAE   | MSE   | RMSE  | R-squared | Explained Variance |
|---------|-------|-------|-------|-----------|---------------------|
| DNN     | 0.027 | 0.001 | 0.033 | 0.986     | 0.994               |
| CNN     | 0.021 | 0.001 | 0.028 | 0.990     | 0.993               |
| LSTM    | 0.0489| --    | 0.0717| --        | --                  |
| XGBoost | 0.026 | 0.001 | 0.032 | 0.987     | 0.993               |

### B. SoH Estimation
For estimating the State of Health (SoH) of electric vehicle batteries, the models DNN, CNN, LSTM, and XGBoost were evaluated based on the Root Mean Square Error (RMSE), which effectively measures the deviation between estimated and actual values of SoH.

| Model   | RMSE  |
|---------|-------|
| DNN     | 0.0275|
| CNN     | 0.055 |
| LSTM    | 0.088 |
| XGBoost | --    |

The results indicate that the DNN model outperformed both the LSTM and CNN in terms of RMSE. The improved efficiency of the DNN is attributed to its flexibility in handling non-sequential data and its ability to model complex relationships between input features and SoH.

## Data

### Battery Data
- **[Battery Data Set (NASA)](https://www.kaggle.com/datasets/patrickfleith/nasa-battery-dataset)**: Contains various battery cycle and aging data, provided by NASA, used for SoC and SoH estimation.
- **[Dataset_Li-ion](https://data.mendeley.com/datasets/wykht8y7tg/1)**: Li-ion battery dataset used for testing and training machine learning models.
- **[LG 18650HG2 Li-ion Battery Data](https://www.researchgate.net/publication/340602691_LG_18650HG2_Lithium-ion_Battery_Dataset)**: Includes data for the LG 18650HG2 battery, including charge/discharge cycles, current, voltage, and temperature readings.

## Usage

### Clone the Repository
To get started with the project, clone the repository using the following command:
```bash
git clone https://github.com/ahmedcherif11/AI-ML-Based-Battery-Management-System-for-EVs.git
cd AI-ML-Based-Battery-Management-System-for-EVs
```

