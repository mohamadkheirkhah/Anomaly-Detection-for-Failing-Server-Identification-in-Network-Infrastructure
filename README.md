# Anomaly-Detection-for-Failing-Server-Identification-in-Network-Infrastructure

## Overview

This project implements an anomaly detection algorithm to identify anomalous behavior in server computers. The algorithm utilizes a Gaussian model to detect anomalies in a 2D dataset and a larger dataset with multiple dimensions. The primary goal is to identify failing servers on a network based on features such as throughput (mb/s) and latency (ms) of server response.

## Dataset

The dataset used in this project comes from the Coursera course by Andrew Ng on Unsupervised Learning. It consists of examples of server behavior, with two features: throughput and latency. The dataset is split into training and cross-validation sets (X_train, X_val, y_val).

## Project Structure

### 1. Imports

The project starts with necessary imports, including NumPy, pandas, Matplotlib, Seaborn, and warnings handling.

### 2. Anomaly Detection

#### 2.1 Problem Statement

The objective is to implement an anomaly detection algorithm using a Gaussian model to identify anomalous behavior in server computers.

#### 2.2 Dataset

The dataset is loaded into variables X_train, X_val, and y_val using NumPy. The dimensions of the variables are displayed, and DataFrames are created for better visualization.

#### 2.3 Gaussian Distribution

The project proceeds to fit a Gaussian distribution to the data. The mean (𝜇) and variance (𝜎^2) for each feature are estimated using the `estimate_gaussian` function. The contours of the fitted Gaussian distribution are visualized using the `visualize_fit` function.

#### 2.4 Selecting the Threshold 𝜖

The threshold 𝜖 is selected using the F1 score on a cross-validation set. The `select_threshold` function iterates over different values of 𝜖 and chooses the one with the highest F1 score.

### 3. High Dimensional Dataset

The project extends the anomaly detection algorithm to a more realistic and challenging dataset with 11 features. The dataset is loaded, and the same steps as in the 2D dataset are applied.

## Running the Code

To run the code, follow these steps:

1. Install the required libraries: NumPy, pandas, Matplotlib, Seaborn.
2. Download the dataset files: X_part1.npy, X_val_part1.npy, y_val_part1.npy, X_part2.npy, X_val_part2.npy, y_val_part2.npy.
3. Execute the code sections in the provided order.

## Results

The algorithm provides information about the best epsilon (𝜖) and the corresponding F1 score. Anomalies are visualized on scatter plots, and the number of anomalies found is displayed.

## Conclusion

This project demonstrates the implementation of an anomaly detection algorithm using a Gaussian model. It is designed to help identify failing servers based on their behavior. The code can be adapted for other datasets and serves as a foundation for anomaly detection tasks.

Feel free to explore and modify the code for your specific use case. If you encounter any issues or have suggestions for improvement, please provide feedback.

## Credits

- This project is inspired by the Unsupervised Learning course by Andrew Ng on Coursera.
