# Healthcare Claims Prior Authorization Auto Approval Model

This project explores how machine learning can help identify prior authorization requests that are very likely to be approved. The goal is to safely automate the simple and predictable cases so that reviewers can focus on requests that need close attention. The dataset is a small, de-identified example that includes prior authorization records and past claim history.

## How the model works
- Combined prior authorization data with claim history using only information available at the time of submission.
- Created features that reflect past behavior, such as count of prior claims, total paid amounts, and days since the last claim.
- Trained three models: Logistic Regression, Random Forest, and XGBoost.
- Tuned and calibrated a Random Forest model, then selected a conservative threshold based on precision.
- Examined results by service type to understand where automation is most reliable.

## Key Results
- Random Forest performed the best on the test set.  
  - AUC: 0.844  
  - Precision: about 0.90  
  - Recall: about 0.73  
  - Threshold used: 0.60  
  - About 53 percent of manual review cases can be safely automated  
- Cross validation showed stable performance with an average AUC of 0.872.

## Files
- PriorAuth_ML_project.ipynb: full workflow
- Data/: de-identified example dataset
- README.md: project overview

## Notes
This dataset is synthetic and used only for demonstration.