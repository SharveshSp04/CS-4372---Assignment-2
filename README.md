# CS-4372---Assignment-2
CS 4372 - HOW TO RUN THE PROGRAM (Assignment) 
Here is a link to the code in Github :
https://github.com/SharveshSp04/CS-4372---Assignment-2.git
Navigate to the Traffic_Flow_Forecasting_Model_Comparison.ipynb file in the GitHub repository
Click on the file to view it
Look for the "Open in Colab" button (typically at the top of the file preview) and click it
This will open the notebook in Google Colab
Run the Entire Notebook:
Once in Google Colab, you can run the entire notebook by going to:
Runtime → Run all in the menu bar
OR run cells individually by clicking the play button (▶️) next to each code cell
Upload the Dataset:
The notebook will automatically prompt you to upload the dataset file
When you see this message:
text
=== UPLOAD TRAFFIC DATASET ===
Please upload your 'traffic_dataset.mat' file when prompted... 
Click the "Choose File" button and select the traffic_dataset.mat file from the GitHub repository
If you can't find the file in the repository, make sure you've downloaded it to your local machine first
Expected Output Sequence
When you run the program successfully, you should see the following outputs in order:
1. Initial Setup Confirmation
text
✅ Libraries imported successfully!
2. Dataset Upload Phase
text
=== UPLOAD TRAFFIC DATASET ===
Please upload your 'traffic_dataset.mat' file when prompted...


traffic_dataset.mat(n/a) - 4401723 bytes, last modified: n/a - 100% done
Saving traffic_dataset.mat to traffic_dataset.mat
Uploaded file: traffic_dataset.mat
3. Data Structure Information
text
Available variables in the .mat file:
  tra_X_tr: (1, 1261) object
  tra_X_te: (1, 840) object
  tra_Y_tr: (36, 1261) float64
  tra_Y_te: (36, 840) float64
  tra_adj_mat: (36, 36) uint8


Selected variable 'tra_Y_tr' as traffic data
Data shape: (36, 1261)
Data type: float64


✅ Dataset loaded successfully!
4. Data Preparation Details
text
=== DATA PREPARATION FOR TRAFFIC FLOW FORECASTING ===
Multivariate data with 1261 features detected
Using first feature column. You can modify this to use other columns or aggregates.
Traffic flow data shape: (36,)
Data range: [0.00, 0.14]
Data mean: 0.06, std: 0.04
Created 28 samples with 8 time steps each


Feature matrix shape: (28, 10)
Target vector shape: (28,)
5. Statistical Summary
text
=== EXPLORATORY DATA ANALYSIS ===
Statistical Summary:
             t-8        t-7        t-6        t-5        t-4        t-3  \
count  28.000000  28.000000  28.000000  28.000000  28.000000  28.000000   
mean    0.069727   0.068426   0.068459   0.067926   0.067458   0.065957   
std     0.036102   0.037437   0.037417   0.037788   0.038163   0.039874   
min     0.009809   0.009809   0.009809   0.009809   0.009809   0.002802   
25%     0.044722   0.044138   0.044138   0.041453   0.034563   0.030593   
50%     0.068192   0.068192   0.068192   0.068192   0.068192   0.068192   
75%     0.096801   0.096801   0.096801   0.096801   0.096801   0.096801   
max     0.140589   0.140589   0.140589   0.140589   0.140589   0.140589  
6. Model Training Progress
text
=== MODEL TRAINING WITH HYPERPARAMETER TUNING ===


=== 1. DECISION TREE REGRESSOR ===
Best parameters: {'max_depth': 3, 'max_features': 'sqrt', 'min_samples_leaf': 1, 'min_samples_split': 2}
Best cross-validation score (Negative MSE): -0.6168


=== 2. RANDOM FOREST REGRESSOR ===
Best parameters: {'max_depth': 5, 'max_features': 'sqrt', 'min_samples_leaf': 1, 'min_samples_split': 2, 'n_estimators': 200}
Best cross-validation score (Negative MSE): -1.2959
7. Visualization Output
Multiple plots will be generated showing:
Feature correlation heatmap
Model performance comparisons
Feature importance charts
Prediction vs actual value plots
8. Final Results Summary
text
=== COMPREHENSIVE RESULT ANALYSIS ===


=== PERFORMANCE METRICS COMPARISON ===
               Model     MSE     MAE    RMSE       R²  MAPE (%)
0      Decision Tree  0.0046  0.0583  0.0681 -29.9451    5.8345
1      Random Forest  0.0016  0.0345  0.0400  -9.6746    3.4499


 BEST PERFORMING MODEL: Decision Tree
   RMSE: 0.0681
   MAE: 0.0583
   R²: -29.9451
   MAPE: 5.83%
9. File Export Confirmation
text
✅ Results saved to 'traffic_forecasting_model_comparison.csv'


============================================================
TRAFFIC FLOW FORECASTING ANALYSIS COMPLETED SUCCESSFULLY!
============================================================
Output Files Generated
Upon successful completion, the program will create:
traffic_forecasting_model_comparison.csv - Contains all model performance metrics and results
Multiple visualization plots - Displayed inline in the notebook
Console output - Detailed analysis results and model comparisons
The entire execution should take approximately 2-5 minutes depending on your system's computational resources, with most of the time spent on hyperparameter optimization for the machine learning models.
