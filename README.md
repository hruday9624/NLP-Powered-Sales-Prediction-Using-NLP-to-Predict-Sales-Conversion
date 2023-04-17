# Text-Enhanced-Sales-Prediction: An-NLP-Approach

This project aims to predict sales based on customer-business executive conversations. We use natural language processing techniques to classify the conversation text into two categories - converted or not converted.

## Dataset
The dataset consists of conversations between customers and business executives. The dataset is preprocessed to remove null values and filled with unknown values in the country column. The status column is cleaned of spelling mistakes and a new binary column, status_id, is created.

## Exploratory Data Analysis
EDA is performed using bar plots, pie charts, heat maps, and maps to visualize lead conversion by lead source, lead status by location, location by lead source, and customer segmentation based on location and status using k-means clustering.

## Model Selection and Evaluation
The dataset is split into training and testing data. Three models - multinomial naive bayes, random forests, and logistic regression - are trained using count vectorization without upsampling. The models are then trained again using count vectorization with upsampling and a third time using TF-IDF vectorization with upsampling. The models are evaluated using precision, recall, and F1 scores.
 
## Model Performance with Different Vectorization and Sampling Techniques

| Technique | Model Accuracy | Precision | Recall |
|-----------|----------------|-----------|--------|
| Count Vectorization Multinomial Naive Bayes | 0.84 | 0.18 | 0.12 |
| Count Vectorization Logistic Regression | 0.87 | 0.12 | 0.3 |
| Count Vectorization Random Forests | 0.88 | 0.25 | 0.03 |
| Count Vectorization with Random Over Sampler Multinomial Naive Bayes | 0.74 | 0.74 | 0.75 |
| Count Vectorization with Random Over Sampler Logistic Regression | 0.84 | 0.80 | 0.91 |
| Count Vectorization with Random Over Sampler Random Forests | 0.95 | 0.93 | 0.99 |
| TF-IDF Vectorization with Random Over Sampler Multinomial Naive Bayes | 0.78 | 0.73 | 0.89 |
| TF-IDF Vectorization with Random Over Sampler Logistic Regression | 0.79 | 0.76 | 0.84 |
| TF-IDF Vectorization with Random Over Sampler Random Forests | 0.96 | 0.92 | 1.0 |


In this table, we compare the performance of different models using different vectorization and sampling techniques. The accuracy, precision, recall, and F1 score were used as evaluation metrics. Count vectorization and TF-IDF vectorization were both used, and random over sampling was applied in some cases to balance the class distribution. Among the models tested, random forests achieved the highest accuracy and F1 score, and the best performance was obtained when using TF-IDF vectorization with random over sampling.
