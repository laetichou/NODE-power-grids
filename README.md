# NODE – Neural Ordinary Differential Equations for Power Grid Dynamics

This project explores methods to accelerate the training of **Neural Ordinary Differential Equation (NODE)** models for predicting the dynamics of power grid systems. The goal is to develop models that are **fast enough for real-time applications while maintaining accurate predictions of system behavior after disturbances**.

## Data format
The raw data should be provided as a tuple containing:
- `time_points`: a 1D tensor of time values
- `data_matrix`: a 2D matrix of shape `(datapoints, features)`

## Pipeline
The workflow consists of three main steps:

1. **Data preprocessing**
   - Configure parameters in `final_data_preprocessing.py`
   - Set:
     - `start`
     - `shifts`
     - `suffixes`
     - `path_root` (path to the raw data)

2. **Run preprocessing**
   - Execute the preprocessing function to clean and scale the data.
   - The processed dataset will be saved to the output directory specified by `path_root`.

3. **Train the model**
   - Open `main.py`
   - Set the `dataset` variable to the file generated during preprocessing
   - Run the script to train the NODE model.

## Features
- Data preprocessing and scaling
- Time-series batching for NODE training
- Hyperparameter tuning and logging
- Metrics including:
  - Mean Squared Error
  - Fréchet Distance
  - Training time

## Repository
GitHub:  
https://github.com/laetichou/NODE-power-grids
