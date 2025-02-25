# Heart-Disease-Classification
# Heart Disease Classification Using Decision Tree and Random Forest Classifiers

## Overview
This project aims to classify the presence of coronary heart disease (CHD) using the Cleveland Heart Disease dataset from the UCI Machine Learning Repository. Two machine learning models are implemented:

- **Decision Tree Classifier (DTC)**
- **Random Forest Classifier (RFC)**

Both models are trained, tested, and compared based on their classification performance and feature importance.

## Dataset
- **Source:** UCI Machine Learning Repository - Cleveland Heart Disease Dataset
- **Link:** [Dataset Link](https://archive.ics.uci.edu/dataset/45/heart+disease)
- **Number of Instances:** 303
- **Number of Features:** 13 input features + 1 target column
- **Target Variable:** `num` (Transformed into `chd` as a binary classification: 0 = No CHD, 1 = CHD)

## Features
- age: Age in years
- sex: Gender (1 = Male, 0 = Female)
- cp: Chest pain type
- trestbps: Resting blood pressure (mm Hg)
- chol: Serum cholesterol (mg/dl)
- fbs: Fasting blood sugar > 120 mg/dl (1 = True, 0 = False)
- restecg: Resting electrocardiographic results
- thalach: Maximum heart rate achieved
- exang: Exercise-induced angina (1 = Yes, 0 = No)
- oldpeak: ST depression induced by exercise relative to rest
- slope: Slope of the peak exercise ST segment
- ca: Number of major vessels colored by fluoroscopy
- thal: Thalassemia status

## Workflow
### 1. Data Loading
- The dataset is loaded using pandas with appropriate column names.
- Missing values are checked and imputed as necessary.
- The `num` column is transformed into a binary column `chd`.

### 2. Data Preprocessing
- No normalization or categorical encoding is performed since the models used (DTC and RFC) do not require it.
- The dataset is split into features (`X`) and target (`y`).

### 3. Train-Test Split
- The dataset is split into training and testing sets using an 80/20 split.

### 4. Model Training and Evaluation
- **Decision Tree Classifier (DTC)**
  - Trained using the training data
  - Performance evaluated using classification report and accuracy score
  - Feature importance visualized using a horizontal bar plot

- **Random Forest Classifier (RFC)**
  - Trained using the training data
  - Performance evaluated using classification report and accuracy score
  - Feature importance visualized using a horizontal bar plot

### 5. Comparison of Results
- The classification performance and feature importance rankings of DTC and RFC are compared.
- Based on accuracy and feature importance consistency, RFC was found to be the better model.

## Results
### Decision Tree Classifier Performance
- Accuracy: 75.41%
- Best predictors: `ca`, `thal`, `cp`

### Random Forest Classifier Performance
- Accuracy: 88.52%
- Best predictors: `ca`, `thal`, `cp`

## File Structure
- `homework2.ipynb`: Jupyter Notebook with the full code and analysis
- `processed.cleveland.data`: Dataset used for the analysis
- `README.md`: This document

## Requirements
- Python 3.11
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - sklearn

Install dependencies using:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Usage
1. Clone the repository:
```bash
git clone <repository-url>
```
2. Navigate to the project directory:
```bash
cd heart-disease-classification
```
3. Open the Jupyter Notebook:
```bash
jupyter notebook homework2.ipynb
```
4. Run all cells to see the results.

## Conclusion
This project demonstrated the effectiveness of Decision Tree and Random Forest classifiers in predicting coronary heart disease. Random Forest outperformed Decision Tree in both accuracy and reliability of feature importance rankings, making it the preferred model for this dataset.

## Author
Tsegie Kassahun

## License
This project is licensed under the MIT License.

