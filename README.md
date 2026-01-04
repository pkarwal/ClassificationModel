# Breast Cancer Classification with K-Nearest Neighbors

A machine learning project that classifies breast tumors as benign or malignant using 
K-Nearest Neighbors (KNN) algorithm. The model achieves 95.1% accuracy on test data by 
analyzing five key tumor characteristics: smoothness, concavity, radius, texture, and perimeter.

 ## Methodology
   
   ### Data Exploration (EDA.ipynb)
   - Analyzed 569 samples with 10 numerical features
   - Found class distribution: 357 Benign (63%) vs 212 Malignant (37%)
   - Created SPLOM visualization to identify feature relationships

  ### Model Building (model.ipynb)
   - Algorithm: K-Nearest Neighbors (KNN)
   - Pipeline: StandardScaler → KNN
   - Train/test split: 75/25 with stratification
   - Hyperparameter tuning: GridSearchCV with 10-fold CV

   ## Results
   
   - **Best K**: 7 neighbors
   - **Cross-validation accuracy**: 97.87%
   - **Test accuracy**: 95.1%
   
   ### Confusion Matrix
   |              | Predicted Benign | Predicted Malignant |
   |--------------|------------------|---------------------|
   | **Benign**   | 86               | 4                   |
   | **Malignant**| 3                | 50                  |
   
   - False Positives: 4 (benign classified as malignant)
   - False Negatives: 3 (malignant classified as benign)

   ## Medical Context & Implications
   
   ### Cost of Errors
   In cancer diagnosis:
   - **False Negatives (3 cases)**: More critical - missing a malignant tumor.
   - **False Positives (4 cases)**: Less critical but causes anxiety, unnecessary procedures.
   
   ### Model Performance Interpretation
   - High accuracy (95.1%) suggests reliable predictions.
   - Low false negative rate (3/53 = 5.7%) is encouraging for medical screening.



