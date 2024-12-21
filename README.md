# Gender Classification Project

This project aims to help me learn SHAP by classifying individuals as male or female based on various physical attributes using machine learning models. The classification has been made intentionally simple for educational purposes. The dataset is obtained from [Kaggle: Gender Classification Dataset](https://www.kaggle.com/datasets/elakiricoder/gender-classification-dataset).

## Project Workflow

### 1. Data Preparation

#### Dataset

The dataset contains the following features:

- **Numerical Features**:
  - `forehead_width_cm`: Width of the forehead.
  - `forehead_height_cm`: Height of the forehead.
- **Categorical Features**:
  - `long_hair`: Binary indicator for long hair.
  - `nose_wide`: Binary indicator for a wide nose.
  - `nose_long`: Binary indicator for a long nose.
  - `lips_thin`: Binary indicator for thin lips.
  - `distance_nose_to_lip_long`: Binary indicator for long distance from nose to lip.
- **Target Variable**:
  - `gender_male`: Binary indicator for gender (1 = Male, 0 = Female).

#### Data Preprocessing

1. **Feature Engineering**:
   - Target column `gender` was mapped to `gender_male` and the original column was dropped.
2. **Train-Test Split**:
   - The dataset was split into training (80%) and testing (20%) sets with stratification.
3. **Feature Scaling**:
   - Numerical and categorical features were scaled using `MinMaxScaler`.

### 2. Model Testing

#### Models Tested

The following machine learning models were tested individually:

1. RandomForestClassifier
2. GradientBoostingClassifier
3. LogisticRegression
4. RidgeClassifier
5. Perceptron
6. SVC (Support Vector Classifier)
7. GaussianProcessClassifier
8. DecisionTreeClassifier
9. KNeighborsClassifier
10. MLPClassifier (Multi-Layer Perceptron)

#### Model Validation

- Models were validated using 3-fold cross-validation with the F1 score as the evaluation metric.
- Results were sorted and displayed based on their average F1 scores.

### 3. SHAP Analysis

#### Local Interpretability

1. **Waterfall Plot**:
   - Visualized the SHAP values for a single prediction to understand how each feature contributed to the model's decision.
2. **Force Plot**:
   - Displayed the combined SHAP values for an individual sample.

#### Global Interpretability

1. **Bar Plot**:
   - Showed the mean absolute SHAP values of the top 10 features to highlight their importance across the dataset.
2. **Beeswarm Plot**:
   - Visualized the distribution of SHAP values for all features, revealing feature importance and potential interactions.
3. **Dependence Plot**:
   - Explored the relationship between a specific feature and its SHAP values, revealing potential interactions with other features.

### Dataset Link

[Gender Classification Dataset on Kaggle](https://www.kaggle.com/datasets/elakiricoder/gender-classification-dataset)
