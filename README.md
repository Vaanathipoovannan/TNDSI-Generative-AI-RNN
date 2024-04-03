# TNDSI-Generative-AI-RNN

# Apple Stock Price Prediction using LSTM

## Introduction
This project aims to forecast the future stock prices of Apple Inc. using Long Short-Term Memory (LSTM) neural networks. The model is trained on historical stock price data and evaluated on a separate testing dataset. LSTM networks are chosen for their ability to capture long-term dependencies in sequential data, making them suitable for time series forecasting tasks.

## Dataset
- Two datasets are used: `Apple_Train.csv` for training and `Apple_Test.csv` for testing.
- Each dataset contains the following columns: Date, Open, High, Low, Close, Adj Close, and Volume.
- The 'Open' column is selected as the feature for prediction.

## Preprocessing
- Data is loaded using Pandas and visualized using Matplotlib and Seaborn.
- The 'Open' column from both datasets is extracted and scaled using MinMaxScaler.
- A data structure is created containing 80 days of historical stock prices for each training instance.

## Model Architecture
- Sequential model with multiple LSTM layers and dropout regularization is constructed using Keras.
- The LSTM layers are stacked to capture complex temporal patterns in the data.
- The output layer consists of a single neuron for predicting the next day's stock price.

## Training
- The model is compiled with Adam optimizer and Mean Squared Error loss function.
- It is trained for 100 epochs with a batch size of 32.

## Testing and Evaluation
- Predictions are made on the test dataset.
- Predicted values are inverse transformed to obtain the actual stock prices.
- Predicted and actual stock prices are plotted for visual comparison.

## Results
- The model demonstrates decent performance in predicting Apple's stock prices, closely following the actual trends.

## Files
- `Apple_Train.csv`: Training dataset
- `Apple_Test.csv`: Testing dataset
- `README.md`: Overview of the project
- `apple_stock_prediction.ipynb`: Jupyter notebook containing the code
