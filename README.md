# Fake-news-prediction

**Overview**
This project aims to detect fake news articles using machine learning techniques, specifically leveraging Logistic Regression. Fake news has become a significant concern in today's digital age, and accurately identifying and filtering out fake news is essential to maintain the integrity of information consumed by the public.

**Dataset**
The dataset used in this project consists of news articles with labels indicating whether an article is real or fake. Each entry in the dataset includes the author's name, the title of the article, and a label (0 for real news, 1 for fake news).

**Components of the Project**
1.Data Collection and Loading
The project begins by collecting a labeled dataset of news articles. Each article in the dataset includes information such as the author, title, and the label indicating whether the news is real or fake. The dataset is loaded into a pandas DataFrame for further processing. Any missing values in the dataset are replaced with empty strings to ensure consistency in the data.

2.Data Preprocessing
To prepare the data for model training, several preprocessing steps are applied:

Combining Features: The author name and news title are merged into a single column called 'content' to form the text that will be analyzed.
Text Cleaning and Stemming: A stemming function is implemented to clean the text data. This function removes non-alphabetic characters, converts text to lowercase, splits the text into individual words, removes stopwords (common words that do not contribute much to the meaning, such as 'the', 'and', etc.), and applies stemming to reduce words to their root form.
Feature and Label Separation: The cleaned text data is separated into features (X) and labels (Y).
Text Vectorization
To convert the textual data into a numerical format suitable for machine learning algorithms, the TfidfVectorizer from scikit-learn is used. This vectorizer transforms the text data into TF-IDF (Term Frequency-Inverse Document Frequency) vectors, which represent the importance of each word in the document relative to the entire dataset.

3.Model Training
The project utilizes logistic regression for binary classification. The dataset is split into training and testing sets to evaluate the model's performance. The logistic regression model is trained on the training set, learning to distinguish between real and fake news based on the provided features.

4.Model Evaluation
The trained model's performance is evaluated using accuracy scores on both the training and test datasets. These scores help determine how well the model generalizes to unseen data. The accuracy on the training data indicates how well the model learned from the training set, while the accuracy on the test data shows its effectiveness in making predictions on new, unseen data.

5.Prediction
To demonstrate the model's capability, a sample news article from the test set is used for prediction. The model predicts whether the news is real or fake, and the result is compared to the actual label. This step showcases the practical application of the model in identifying the authenticity of news articles.
