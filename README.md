NSAP Predominant Scheme Prediction

Overview: This project develops a machine learning model to predict the most prevalent National Social Assistance Program (NSAP) scheme for a given district and financial year in India. Using an aggregated dataset, the model helps government agencies make data-driven decisions.

Goal: To provide an automated tool for:
 1. Predictive Resource Planning: Anticipate future scheme needs.
 2. Informed Policy Decisions: Understand demogrphic factors influencing scheme demand.
 3. Data Auditing: Automatically flag data anomalies.
   
Methodology: The project follows a standard machine learning workflow using Python and IBM Watson Studio:
 1. Data Preprocessing: Cleaned and transformed the nsapallschemes.csv dataset, creating a new target variable for the predominant scheme.
 2. Model Building: A RandomForestClassifier was trained using an sklearn pipeline.
 3. Evaluation & Refinement: The model was evaluated for accuracy and refined by comparing it to other models and using hyperparameter tuning.
  
Key Features:
1. Predictive Insights: Anticipates future scheme demands.
2. Actionable Guidance: Explains model predictions to inform policy.
3. Anomaly Detection: Flags potential data errors.

Technologies:
1. Platform: IBM Cloud, IBM Watson Studio
2. Libraries: pandas, scikit-learn, matplotlib, joblib
  
How to Use the Project:
1. Reproduce the Notebook
   1. Setup: Create a free IBM Cloud account and provision an IBM Watson Studio service.
   2. Files: Create a project in Watson Studio and upload the nsapallschemes.csv file.
   3. Run: Create a new Jupyter Notebook, copy the project code into it, and run all cells sequentially.
3. Make New Predictions
   1. Load: Load the saved nsap_predominant_scheme_pipeline.joblib and nsap_predominant_scheme_label_encoder.joblib files.
   2. Prepare Data: Create a new Pandas DataFrame with the same columns as the model's training data.
   3. Predict: Use the loaded pipeline's .predict() method on your new data.
   4. Interpret: Use the label encoder's inverse_transform() to convert the numerical prediction back into the scheme name.
