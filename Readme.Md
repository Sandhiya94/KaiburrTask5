###  Task 5: Text Classification on Consumer Complaint Dataset

In this task, we performed text classification on the consumer complaint dataset available [here](https://catalog.data.gov/dataset/consumer-complaint-database) into the following categories:

- 0: Credit reporting, repair, or other
- 1: Debt collection
- 2: Consumer Loan
- 3: Mortgage

#### Steps Involved:

1. **Explanatory Data Analysis and Feature Engineering**:
   - Loaded the dataset `complaints.csv` containing consumer complaints.
   - Explored the dataset to understand its structure, features, and distribution.
   - Filtered the dataset to include only relevant categories: Mortgage, Credit reporting, Credit repair services, Consumer Loan, and Debt collection.
   - Selected relevant features for classification, including 'Consumer complaint narrative' and 'Product'.
   - Handled missing values by dropping rows with NaN values in the selected features.
2. **Text Pre-Processing**:
   - Pre-processed the text data by removing stopwords.
   - Applied feature extraction techniques such as TF-IDF (Term Frequency-Inverse Document Frequency) to convert text data into numerical features.
   - Performed feature selection using SelectKBest with chi-squared test to select the top features.
3. **Selection of Multi-Classification Model** **and comparison of models**:
   - Compared the performance of various classification models using pipelines, including Random Forest, Logistic Regression, K-Nearest Neighbors, Support Vector Machine, and Naive Bayes.
   - Trained each model on the pre-processed text data.
   - Evaluated the models using accuracy score.
4. **Model Evaluation**:
   - Selected Random Forest and Support Vector Machine models based on their higher accuracy scores.
   - Evaluated the selected Random Forest model using cross-validation to ensure robustness.
   - Visualized the confusion matrix to understand the model's performance on each category.
5. **Prediction**:
   - Defined a sample text for inference.
   - Vectorized the sample text using the trained TF-IDF vectorizer and selected top features.
   - Loaded the trained Random Forest model using pickle.
   - Predicted the category of the sample text using the loaded model and inverse transformed the prediction to get the actual product category.

