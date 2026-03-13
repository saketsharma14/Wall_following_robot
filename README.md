# Wall-Following Robot Navigation --- Machine Learning Model Comparison

## Overview

This project evaluates multiple machine learning models for predicting
the movement direction of a wall-following robot using sensor data.

The robot is equipped with distance sensors that measure proximity to
surrounding walls. Based on these readings, the goal is to predict the
robot's next navigation action.

The project compares the performance of several classification
algorithms and analyzes which model performs best for this task.

------------------------------------------------------------------------

# Problem Statement

A robot navigating along walls must decide its next movement direction
based on sensor readings.

Possible navigation actions:

-   Slight-Right-Turn\
-   Sharp-Right-Turn\
-   Move-Forward\
-   Slight-Left-Turn

The objective is to train machine learning models that can accurately
predict these actions from sensor inputs.

------------------------------------------------------------------------

# Dataset

The dataset contains sensor measurements from a wall-following robot.

Each observation includes distance readings from multiple sensors placed
around the robot. These measurements are used as input features for the
classification models.

The target variable represents the robot's next movement direction.

Key characteristics:

-   Multiclass classification problem
-   Class imbalance present in the dataset
-   Numerical sensor features

------------------------------------------------------------------------

# Project Workflow

## 1. Data Exploration

-   Loaded and inspected the dataset
-   Analyzed class distribution
-   Examined feature statistics

## 2. Baseline Models

Two baseline approaches were implemented:

-   **Majority Class Predictor**
-   **Random Prediction Baseline**

These baselines help determine whether trained models perform
meaningfully better than naive approaches.

## 3. Model Training

The following machine learning models were implemented and evaluated:

-   Logistic Regression
-   Decision Tree
-   Random Forest
-   Multi-Layer Perceptron (MLP)

All models were implemented using **scikit-learn**.

## 4. Model Evaluation

Models were evaluated using:

-   **Macro F1 Score**
-   **Accuracy**
-   **Confusion Matrices**

Macro-F1 was used because it treats all classes equally and is
appropriate for imbalanced datasets.

## 5. Model Analysis

Additional analysis included:

-   Confusion matrix visualization
-   Training convergence analysis (Logistic Regression)
-   Feature importance analysis for Random Forest

------------------------------------------------------------------------

# Results

Among the evaluated models, **Random Forest achieved the best
performance**.

Key observations:

-   Random Forest achieved **0.99 Macro F1 Score**
-   Ensemble methods performed better than individual models
-   Feature importance analysis identified the most informative sensors
    for navigation decisions

These results suggest that tree-based ensemble models are well-suited
for this structured sensor dataset.

------------------------------------------------------------------------

# Technologies Used

-   Python
-   NumPy
-   pandas
-   scikit-learn
-   Matplotlib

------------------------------------------------------------------------

# Repository Structure

    wall-following-ml/
    │
    ├── notebook.ipynb        # Main project notebook
    ├── README.md             # Project documentation
    └── dataset/              # Robot sensor dataset

------------------------------------------------------------------------

# Example Visualizations

The notebook includes visualizations such as:

-   Confusion matrices for model evaluation
-   Training convergence plots
-   Feature importance rankings for the Random Forest model

These visualizations help interpret model performance and understand
which sensors influence predictions the most.

------------------------------------------------------------------------

# Key Takeaways

-   Ensemble models like **Random Forest** perform strongly on
    structured sensor data.
-   Proper evaluation metrics such as **Macro F1** are important when
    dealing with class imbalance.
-   Feature importance analysis can provide insights into which sensor
    readings drive navigation decisions.

------------------------------------------------------------------------

# Future Improvements

Possible extensions of this project include:

-   Hyperparameter tuning using GridSearchCV
-   Cross-validation for more robust evaluation
-   Model interpretability using SHAP values
-   Real-time inference for robotic navigation systems

------------------------------------------------------------------------

# Author

Saket Sharma\
B.Tech Computer Science and Engineering\
IIT Delhi Abu Dhabi
