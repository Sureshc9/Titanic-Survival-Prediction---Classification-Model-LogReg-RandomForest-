# Titanic-Survival-Prediction---Classification-Model-LogReg-RandomForest-
This project uses Logistic Regression and Random Forest to predict Titanic passenger survival, covering data cleaning, EDA, model training, and performance evaluation with ROC and gains charts a full classification workflow in Python.

# Dataset Overview"

  •	Source: https://web.stanford.edu/class/archive/cs/cs109/cs109.1166/problem12.html
	
  •	Rows: ~891
	
  •	Features: Age, Sex, Pclass, SibSp, Parch, Fare, and Survived

# Project Workflow:

  Step 1: Data Cleaning
	•	Replaced missing Age values with median
	•	Renamed columns for readability
	•	Encoded categorical features (Sex)
	•	Binned continuous features (Age, Fare) into deciles

 Step 2: Exploratory Data Analysis (EDA)
 
 • Histograms & Frequency Distributions
 
  ![Unknown](https://github.com/user-attachments/assets/d302bfda-1764-4e91-a3f3-88c88b40c942)

 • Marginal Survival Rates by Quantiles

  ![Unknown-2](https://github.com/user-attachments/assets/b907535c-49ec-42ac-8556-7084eaae2727)


# Models Built:

 > Logistic Regression
	•	max_iter=1000
	•	Simple and interpretable
	•	Fast to train

 > Random Forest Classifier
	•	n_estimators=100, max_depth=5
	•	Captures non-linear relationships
	•	Handles variable importance well

# Model Evaluation:

  ROC Curves (AUC Score)
  <img width="244" alt="Screenshot 2025-05-05 at 9 04 33 PM" src="https://github.com/user-attachments/assets/a49ec874-a7d4-4bf5-a989-986fbd8da1e4" />
  
  ![Unknown-3](https://github.com/user-attachments/assets/27da6fca-893c-4800-b559-054b93aaf54c)


  Gains Charts

  ![Unknown-4](https://github.com/user-attachments/assets/3e7ab221-3b14-4859-ab3d-479e9e6a1ba1)

  
  ![Unknown-5](https://github.com/user-attachments/assets/5d84ba68-af53-48ef-8059-c17766c34849)


# Feature Set Used:

  features = ["Pclass", "Sex", "Age", "SibSp", "Parch", "Fare"]

# Summary:

  • Logistic Regression is effective but limited in modeling complex relationships
	•	Random Forest outperforms with a better AUC and gains curve
	•	Clear survival trends: young passengers and high-fare payers had better survival chances

# Future Enhancements

  • GridSearchCV for hyperparameter tuning
	•	Add Cabin, Embarked, and interaction features
	•	Use XGBoost/LightGBM for performance benchmarks
	•	Deploy as Streamlit or Flask app
	
