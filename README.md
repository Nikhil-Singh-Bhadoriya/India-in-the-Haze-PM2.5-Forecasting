# India-in-the-Haze-PM2.5-Forecasting


Overview
This project focuses on forecasting short-term PM2.5 concentrations across India using scientific machine learning models.

Problem Statement
India faces severe air pollution challenges, with PM2.5 levels often exceeding safe limits. Accurate forecasting enables timely interventions and reduces health risks.

Dataset
Source: WRF-Chem simulations
Training: 2016 (April, July, October, December)
Testing: 2017 (unseen months)
Spatial Resolution: 140 x 124 grid
Temporal Features:
PM2.5: 10 past timesteps
Other variables: 26 timesteps (past + future)
My Approach
This solution is based on:

Convolutional layers, Transformer-based modeling
Spatio-temporal modeling of PM2.5 as grid-based data
Leveraging meteorological features along with historical PM2.5
Training on multi-season data to capture diverse patterns
Key Steps
Data Loading from provided NumPy files
Custom train-validation split
Feature selection and preprocessing
Model training on spatio-temporal data
Inference on test dataset
Saving predictions in required format
Model Insights
Captures spatial dependencies across India grid
Learns temporal evolution of pollution
Uses auxiliary meteorological variables for better accuracy
Evaluation
Metric: RMSE (Root Mean Square Error)
Lower RMSE indicates better performance
Submission Format
File: preds.npy
Shape: (996, 140, 124, 16)
Location: /kaggle/working/
Impact
A reliable PM2.5 forecasting system can:

Protect public health
Enable early warnings
Assist policymakers
Reduce economic losses
How to Run
Open the notebook
Run all cells sequentially
Ensure dataset paths are correct
Generate preds.npy
Future Improvements
Physics-informed ML models
Transformer-based architectures
Ensemble methods
Real-time deployment
