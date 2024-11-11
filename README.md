### Project Description: Quora Insincere Questions Classification

#### 1. Statement of the Problem
The primary task is to identify which content is toxic in order to improve online communication on the Quora platform

#### 2. Sources and Description of Data
The dataset used for this project is sourced from the Kaggle competition titled "Quora Insincere Questions Classification." The dataset can be accessed [here](https://www.kaggle.com/c/quora-insincere-questions-classification).

- **Data Structure**: The dataset consists of two main columns:
  - `question_text`: The text of the question (string).
  - `target`: A binary label indicating whether the question is insincere (1) or sincere (0).

- **Types of Variables**:
  - `question_text`: Object (string)
  - `target`: Integer (0 or 1)

The dataset contains approximately 130,612 rows.


#### 3. Approach to the Solution
The methodology for solving the classification task involves several key steps:

- **Data Preprocessing**: Includes text normalization techniques such as `tokenization`, `removal of stop words`, and `stemming` to prepare the text for analysis.
  
- **Feature Extraction**: The Bag of Words (`BoW`) model and Term Frequency-Inverse Document Frequency (`TF-IDF`) model are employed to convert the text data into numerical vectors suitable for machine learning.

- **Model Selection**: 
  - Logistic Regression

- **Evaluation Metrics**: The performance of the models is evaluated using accuracy and F1-score

- **Tools and Libraries**: The project utilizes Python libraries such as Pandas for data manipulation, NLTK for natural language processing, Scikit-learn for machine learning

#### 4. Obtained Results and Conclusions
The analysis and model training resulted in a logistic regression model with BoW vectorisation achieving an `accuracy of approximately 95%` and `f1 score 0.45` on the training data, indicating a strong capability to classify insincere questions. 

The confusion matrix shows that while the model performs well in identifying sincere questions, there are some misclassifications in the insincere category, highlighting potential areas for improvement.

**Findings**:
- The model effectively reduces the volume of toxic content presented to users, thus addressing the initial problem statement.
- The analysis revealed that certain keywords and phrases are strong indicators of insincerity, which can be leveraged for further model improvements.

**Suggestions for Improvement**:
- Experiment with advanced models such as deep learning approaches (e.g., LSTM, BERT) to capture more complex patterns in the text.
- Implement cross-validation to ensure the model's robustness and generalizability across different subsets of the data.
- Consider augmenting the dataset with additional sources of insincere content to improve model training.
