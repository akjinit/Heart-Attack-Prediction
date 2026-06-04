# Heart Attack Prediction

This repository contains a Kaggle-based Jupyter notebook that performs exploratory data analysis and machine learning modeling to predict whether a patient has had a heart disease event or heart attack.

## Project Overview

The notebook `heart-attack-prediction-5d678a.ipynb` covers the full machine learning workflow:

1. Data loading
   - Reads the `heart_disease_health_indicators.csv` dataset from the Kaggle input path.
   - The dataset contains binary health indicators and demographic features for each patient.

2. Exploratory Data Analysis (EDA)
   - Prints dataset statistics, data types, and value counts for key variables.
   - Verifies that there are no missing values.
   - Builds visualizations:
   
     - correlation heatmap
     - count plots for sex and heart disease occurrence
     - distribution plots for age and BMI by heart disease label
     - comparisons of smoking and physical activity against heart disease outcomes

3. Model training
   - Splits data into training and testing sets.
   - Creates a preprocessing pipeline for numeric and categorical data.
   - Uses `LogisticRegression` as the baseline classification model.
   - Evaluates model performance with accuracy, classification report, and confusion matrix.

4. Imbalanced dataset handling
   - Detects that the dataset is imbalanced for the heart disease class.
   - Applies SMOTE oversampling inside a pipeline to improve prediction balance.
   - Re-evaluates results after resampling.

## Dataset

The notebook uses the Kaggle dataset: `heart_disease_health_indicators.csv` from the `heart-disease-indicators` dataset. Key features include:

- `HeartDiseaseorAttack` - target label (0 or 1)
- `BMI`
- `Smoking`
- `AlcoholDrinking`
- `Stroke`
- `PhysicalHealth`
- `MentalHealth`
- `DiffWalking`
- `Sex`
- `Age`
- `Education`
- `PhysicalActivity`
- `GenHealth`
- `SleepTime`
- `Asthma`
- `KidneyDisease`
- `SkinCancer`

## Dependencies

Install the required Python packages before running the notebook:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn notebook
```

## How to run

1. Install dependencies.
2. Launch Jupyter Notebook in the project folder.

```bash
jupyter notebook
```

3. Open `heart-attack-prediction-5d678a.ipynb`.
4. Run the notebook cells sequentially.

