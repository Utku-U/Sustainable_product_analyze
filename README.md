# Sutainable_Product_Analyze

This project presents a machine learning framework that predicts whether a product is commercially and ecologically "optimum" by analyzing the balance between metrics and economic constraints on a synthetic dataset.

This project focuses on analyzing a synthetic dataset of sustainable products. The primary objective is to experiment with various machine learning models on the dataset while strictly adhering to the standard data analysis phases to extract meaningful and actionable insights.

## **Business Problem:**

- This involves using machine learning and deep learning models (both Wide and deep Model) to predict whether a product is commercially viable (optimum) under all environmental and economic constraints.
- What are the three most important factors that ensure Is_Optimum=Yes?

## Dataset and Preprocessing

- Data Cleaning: Descriptive variables with high cardinality and low predictive power, such as Product ID and Product Name, have been removed from the dataset.
- Type Conversion: For memory management and model performance, variables containing a limited number of unique values ​​have been converted to the category type.

## Models

- Base Model (Decision Tree): A reference point is created with the max_depth=3 parameter to ensure the model's interpretability and to control for overfitting.
- Ensemble Learning: * Voting Classifier: A hybrid prediction mechanism has been created by combining Logistic Regression, SVM, and Decision Trees.
- Deep Learning (Wide and Deep Learning): A custom neural network architecture has been designed on Keras/TensorFlow for memorizing categorical data (Broad) and generalizing numerical data (Deep).

## Results
The models are evaluated based on test data and OOB (Out-of-Bag) scores as follows:

| Model | Accuracy 
| :--- | :---: | 
| **Bagging Classifier (OOB)** | **%94.8** | 
| Voting Classifier | %90.5 | 
| Bagging Classifier | %86.8 |
| Wide and Deep | %82.0 | 
| Decision Tree (Baseline) | %80.3 | 
| Random Forest | %77.7 | 

### **Bagging Classifier Detaylı Performans Raporu**

**Genel Test Doğruluğu (Accuracy):** `%94.83`

| Class / Metric | Precision | Recall | F1-Score | Support |
| :--- | :---: | :---: | :---: | :---: |
| **0 Not Optimum** | 0.95 | 0.98 | **0.96** | 7106 |
| **1 Optimum** | 0.95 | 0.89 | **0.92** | 3379 |
| | | | | |
| **Accuracy** | - | - | **0.95** | 10485 |
| **Macro Avg** | 0.95 | 0.93 | 0.94 | 10485 |
| **Weighted Avg** | 0.95 | 0.95 | **0.95** | 10485 |


## Setup
pip install -r requirements.txt

## Source & Domain information
https://data.world/jash1804/sustainable-product-optimization-dataset-spod/workspace/project-summary?agentid=jash1804&datasetid=sustainable-product-optimization-dataset-spod
