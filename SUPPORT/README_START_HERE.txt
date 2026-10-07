RANDOM FOREST MACHINE LEARNING PROJECT - COMPLETE PACKAGE
==========================================================

Project: Diabetes Prediction Using the Pima Indians Diabetes Dataset
Algorithm: Random Forest Classification
Dataset source: https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database
Dataset size: 768 rows, 8 predictor features, 1 binary target (Outcome)

SUBMISSION FILES
----------------
The SUBMIT folder is ready as-is and contains:
1. Random_Forest_Diabetes_Project.ipynb - fully executed Jupyter Notebook with code, comments, outputs, evaluation, plots, feature importance, cross-validation, tuning, model saving and conclusion.
2. Random_Forest_Project_Report.pdf - professional one-page project report, matching the given submission format.
3. diabetes.csv - local copy of the dataset used so the notebook can run without downloading anything.

SUPPORT FILES
-------------
The SUPPORT folder contains generated evidence/output files:
- confusion_matrix.png
- roc_curve.png
- feature_importance.png
- evaluation_metrics.csv
- feature_importance.csv
- random_forest_diabetes_model.joblib
- Viva_Quick_Notes.txt
- requirements.txt

REPRODUCIBILITY
---------------
The notebook was executed end-to-end successfully with no cell errors. It uses a fixed random_state=42 and a stratified 80/20 train-test split. Hyperparameter tuning uses stratified 5-fold GridSearchCV with ROC-AUC scoring.

FINAL TEST RESULTS
------------------
Accuracy : 75.32%
Precision: 69.05%
Recall   : 53.70%
F1-Score : 60.42%
ROC-AUC  : 81.04%
Confusion matrix: TN=87, FP=13, FN=25, TP=29
Best 5-fold CV ROC-AUC: 0.8304
Mean 5-fold CV Accuracy: 0.7642

BEST RANDOM FOREST SETTINGS
---------------------------
n_estimators=300
max_depth=8
min_samples_leaf=2
max_features='sqrt'
min_samples_split=2
random_state=42

IMPORTANT DATA-CLEANING CHOICE
------------------------------
The dataset records some physiologically invalid zeros in Glucose, BloodPressure, SkinThickness, Insulin and BMI. These are converted to missing values and median-imputed inside the modeling pipeline. All predictors are numeric, so categorical encoding is correctly documented as not required.

Educational project only; the model is not a clinical diagnostic system.
