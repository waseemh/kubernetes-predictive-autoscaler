# Kubernetes Predictive Autoscaler

Predictive Horizontal Pod Autoscaler based on statistical and deep learning models. 

## Overview

Kubernetes Horizontal Autoscaler (HPA) works in a reactive manner. Resources usage is evaluated by various metrics at specific intervals, and scaling occurs when the preset threshold is exceeded. Such approach imposes a limitation as scaling decisions are not immediate.

When using a proactive autoscaling approach based on predictive modeling, we solve the latency problem caused by HPA by predicting usage at a specific time and perform the autoscaling beforehand.

The predictive autoscaler leverages statistical models (Linear Regression, Holt-Winters Smoothing) to predict the number of pod replicas at a specific point in time.

To increase the prediction forecast accuracy, we use a deep learning model based on Bi-LSTM (Bidirectional LSTM) recurrent neural network.
