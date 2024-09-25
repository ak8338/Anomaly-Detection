# Efficient Data Stream Anomaly Detection

This project involves developing a Python script that detects anomalies in a continuous data stream, simulating real-time metrics such as financial transactions or system performance.

Project Overview
The goal of this project is to implement an efficient algorithm for detecting unusual patterns in streaming data. The solution adapts to concept drift and seasonal variations, ensuring accurate anomaly detection in real time.

Key Features:
Data Stream Simulation: A Python function that generates a continuous stream of floating-point numbers, including regular seasonal patterns, random noise, and injected anomalies.
Anomaly Detection Algorithm: The Exponentially Weighted Moving Average (EWMA) algorithm is implemented to track and detect anomalies based on deviations from expected values.
Efficiency: The algorithm is optimized for speed and efficiency, using minimal external resources.
Robustness: Includes thorough error handling and data validation to ensure the solution is reliable.

Algorithm
The EWMA (Exponentially Weighted Moving Average) algorithm tracks a weighted average of data points, prioritizing recent data while still considering historical values. This makes it highly effective in detecting anomalies in data streams that exhibit gradual changes over time.

Steps:
1. Initialization - The first value of the data stream is used to initialize the EWMA.
2. Update - For each subsequent data point, a new EWMA value is computed using the formula: EWMA_new = alpha * data_new + (1 - alpha) * EWMA_old
3. Anomaly Detection - If the absolute difference between the current data point and the EWMA exceeds a predefined threshold, the data point is flagged as an anomaly.
