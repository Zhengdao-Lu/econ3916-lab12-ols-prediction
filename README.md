# econ3916-lab12-ols-prediction
OLS as a Line of Best Fit: Estimation versus Prediction
Objective
I compared how OLS estimates relationships and predicts outcomes for districts the model has not seen.
Methodology
- I fitted the same line using the closed form, statsmodels, and scikit-learn.
- I added up to 100 noise columns and tracked R-squared and adjusted R-squared.
- I split the data before fitting an eight-feature model and compared its training and test RMSE.
- I estimated the AveRooms coefficient and its 95% confidence interval, then measured the specification’s test RMSE.
- I used holdout_rmse() to score median income alone on held-out rows.
Key Findings
All three methods gave the same slope, 0.417938. R-squared rose from 0.4734 with no noise columns to 0.4758 with 100, while adjusted R-squared fell to 0.4732 with 100 columns.

The eight-feature model had training RMSE 0.7197 and test RMSE 0.7456. The AveRooms coefficient was −0.0381, with a 95% confidence interval of [−0.0430, −0.0333]. The two-feature specification had test RMSE 0.8379, and median income alone had test RMSE 0.8421.

