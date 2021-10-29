# Welcome to the Class_Imbalance_SMOTE Repo!

### What is this repo about?
The 'class imbalance' problem is a characteristic of real-world data. This occurs when the one class is over- or under-represented in a categorical variable. This causes ML models to learn biased representation of the over-represented class, making predicting the under-represented class nearly impossible at best. As such, this study aimed to illustrate the impact to ML performance metrics before versus after the predictor variable was balanced using synthetic data. 

### Data, ML Models, and Overal Conclusion
The dataset studied is the real-world *"Diabetes 130-US hospitals for years 1999-2008 Data Set"* sourced from UCI. It contains real records of diabetes patients and an indication of whether or not each patient was readmitted to hospital within 30 days. As such, I trained six ML models to classify/predict whether or not a patient will be readmitted to hospital as this has serious cost- and health-related implications.

Six ML classifiers (SVM, GNB, kNN, LogReg, XGBoost, and RF) were compared across 5 key metrics (F1 score, accuracy, recall, precision, and ROC/AUC) and trained in two parallel experiments. In the first experiment, I trained all models on the unbalanced readmissions (yes/no) variable. Then, I applied the SMOTE (synthetic minority oversampling) package to balance the predictor variable. This caused the balance of yes/no readmission to change in proportions from 90/10 to 50/50. As such, I repeated the ML experiment on the balanced dataset, and reported the results.

> Spoiler Alert
All six models achieved improved scores for all five classification metrics when trained on the post-SMOTE balanced dataset. 

### What does this repo contain?
- **Diabetes_UCI.ipynb**: This notebook shows all my data pre-processing, EDA, and model development/training.
- **README.md**: Hello, you're reading me!
- **UCI_diab.png**": picture of the UCI dataset website.
- **models_perf_bal.png**: Metrics for all six models trained on the SMOTE-balanced dataset.
- **models_perf_imbal.png**: Metrics for all six models trained on the raw imbalanced dataset.
