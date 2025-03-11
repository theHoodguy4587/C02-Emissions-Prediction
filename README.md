# CO2 Emissions Prediction - Data Science Project

## Project Overview

This project focuses on analyzing and predicting CO2 emissions by vehicles based on various features. The dataset used is taken from the official Canada Government open data website and contains details on how CO2 emissions can vary with different vehicle characteristics over a period of 7 years.

The main goal of this project is to:
- Perform **Exploratory Data Analysis (EDA)** to understand the data.
- Apply **preprocessing** techniques such as encoding and scaling.
- Build and evaluate a **Random Forest** model to predict CO2 emissions.

## Dataset Description

The dataset consists of 7385 rows and 12 columns. The features in the dataset are:

- **Model**: Various vehicle models with features like 4WD/4X4, AWD, FFV, etc.
- **Transmission**: Types of transmission such as Automatic (A), Automated Manual (AM), etc.
- **Fuel type**: Type of fuel used by the vehicle (e.g., Regular Gasoline, Diesel, Ethanol, etc.)
- **Fuel Consumption**: City and highway fuel consumption ratings in liters per 100 kilometers (L/100 km) and miles per gallon (mpg).
- **CO2 Emissions**: The tailpipe emissions of CO2 in grams per kilometer for combined city and highway driving.

### Abbreviations Used:
- **4WD/4X4**: Four-wheel drive
- **AWD**: All-wheel drive
- **FFV**: Flexible-fuel vehicle
- **SWB**: Short wheelbase
- **LWB**: Long wheelbase
- **EWB**: Extended wheelbase

### Transmission:
- **A**: Automatic
- **AM**: Automated manual
- **AS**: Automatic with select shift
- **AV**: Continuously variable
- **M**: Manual
- **3 - 10**: Number of gears

### Fuel Type:
- **X**: Regular gasoline
- **Z**: Premium gasoline
- **D**: Diesel
- **E**: Ethanol (E85)
- **N**: Natural gas

## Problem Statement

The primary questions we are addressing in this project are:
1. What are the most influential features affecting CO2 emissions?
2. How do the separate fuel consumption variables for city and highway compare to the combined variable in terms of their influence on CO2 emissions?

## Project Workflow

### 1. Data Loading and Preprocessing
- **Data Cleaning**: The dataset is loaded, and missing values are handled.
- **Categorical Encoding**: Categorical variables such as `Model`, `Transmission`, and `Fuel type` are encoded using techniques like one-hot encoding or label encoding.
- **Feature Scaling**: Numerical features like fuel consumption are scaled using the **StandardScaler** to normalize their ranges, ensuring that they are on the same scale for the model.
- **Train-Test Split**: The dataset is split into training and testing sets to evaluate the model's performance.

### 2. Exploratory Data Analysis (EDA)
- **Data Visualization**: Visualizations are created to understand the distribution of CO2 emissions and relationships between features.
- **Correlation Analysis**: Correlation between different features is analyzed to identify the most influential ones on CO2 emissions.
- **Outlier Detection**: Outliers are checked, and necessary transformations are applied to improve model performance.

### 3. Model Building
- **Random Forest Regressor**: A Random Forest model is trained using the preprocessed data.
- **Model Training**: The model is trained on the training data and evaluated on the test data.

### 4. Model Evaluation
- Performance metrics such as **Mean Absolute Error (MAE)** and **R-squared (R²)** are used to evaluate the model's accuracy and predictive power.

### 5. Hyperparameter Tuning
- **GridSearchCV** is used for hyperparameter tuning to optimize the Random Forest model for better performance.

## Key Findings
- The **most influential features** affecting CO2 emissions are identified.
- A comparison is made between using **separate fuel consumption variables** for city and highway driving and the **combined weighted variable**.

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

To install the dependencies, run:

```bash
pip install -r requirements.txt
```
## Conclusion
- The Random Forest model has been successfully used to predict CO2 emissions.
- Key features that influence CO2 emissions were identified, and insights were drawn from the comparison of fuel consumption data.

## Acknowledgements
The dataset has been sourced from the Canada Government Open Data Website.
