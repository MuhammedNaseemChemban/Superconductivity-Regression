# Predicting Superconducting Critical Temperature: A Machine Learning Approach

## Name: MUHAMMED NASEEM CHEMBAN
## Date: 21/03/2025

## Overview of Problem Statement
Superconductors exhibit zero electrical resistance below a certain temperature, known as the critical temperature (Tₖ). Identifying new superconducting materials with high Tₖ is crucial for advancements in energy transmission, magnetic levitation, and quantum computing. However, traditional experimental methods for discovering new superconductors are time-consuming and costly.

This project aims to leverage machine learning (ML) techniques to predict the critical temperature of superconductors based on their features. The dataset includes 82 features, extracted from material properties, and feature selection is performed using SelectKBest to enhance model performance. By developing a predictive ML model, this research contributes to accelerating the discovery of new superconducting materials, reducing reliance on expensive and time-intensive laboratory experiments.

## Objective
The objective of this project is to develop a machine learning model capable of accurately predicting the critical temperature (Tₖ) of superconductors based on their material properties. This will help in:

- **Enhancing Material Discovery**: Utilizing data-driven techniques to identify potential superconducting materials efficiently.
- **Reducing Experimental Costs & Time**: Minimizing the need for expensive and time-consuming laboratory experiments by providing reliable predictions.
- **Improving Feature Selection & Model Performance**: Using techniques like SelectKBest to identify the most relevant features, ensuring an optimized and interpretable model.
- **Advancing Materials Informatics**: Bridging physics and machine learning to develop computational tools for superconductor research.

By achieving these objectives, this project contributes to the broader goal of accelerating superconductor discovery and supporting advancements in energy transmission, quantum computing, and other cutting-edge technologies.

## Data Description
- **Source**: Superconductivity Dataset - UCI Machine Learning Repository
- **Dataset link**: [Superconductivity Data](https://archive.ics.uci.edu/dataset/464/superconductivty+data)

## Features
The dataset consists of 82 features extracted from the chemical composition of superconducting materials. These features include:

- **Atomic Properties**: Average atomic weight, electronegativity, atomic radius, and valency.
- **Electronic Structure**: Density of states, Fermi energy, and ionization energy.
- **Material Composition**: Fractional presence of different elements in the compound.
- **Target Variable (Tₖ)**: The critical temperature at which the material transitions into a superconducting state.

The goal of the project is to use these features to predict the critical temperature of superconductors with high accuracy using machine learning techniques.

## Initial Insights from the Data
- **Dataset Size**: 21,263 rows and 82 columns.
- **Target Variable**: critical_temp (Critical Temperature) is a continuous numerical variable.

## Model & Methodology
1. **Data Preprocessing**
   - Handled missing values by imputing the median.
   - Standardized the data using **StandardScaler**.
   - Selected the best features using **SelectKBest**.

2. **Machine Learning Models Used**
   - Random Forest Regressor (Best-performing model)
   - Gradient Boosting Regressor
   - Support Vector Regressor

3. **Model Evaluation Metrics**
   - Mean Absolute Error (MAE): **0.1604**
   - Mean Squared Error (MSE): **0.0669**
   - Root Mean Squared Error (RMSE): **0.2586**
   - R² Score: **0.9334**

## Conclusion
- The project successfully implemented machine learning models to predict the critical temperature of superconductors.
- Feature selection and scaling improved the model’s efficiency and accuracy.
- The best-performing model provides a data-driven approach to superconductor discovery, minimizing experimental costs and accelerating material research.
- The predicted values were initially in the transformed scale due to preprocessing. To obtain the predictions in the original dataset range, we applied the inverse transformation using **PowerTransformer**. This ensured that the predicted critical temperatures were mapped back to their actual physical values, making them interpretable in the real-world context of superconductivity.

## Future Scope
- Experimenting with deep learning models like neural networks for improved predictions.
- Exploring additional feature engineering techniques to enhance model interpretability.
- Applying the trained model to real-world material discovery scenarios.
