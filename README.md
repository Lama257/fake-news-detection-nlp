\# Fake News Detection Using NLP



An NLP-based fake news detection project that applies traditional machine learning, deep learning, and transformer-based models to classify news articles as \*\*Fake\*\* or \*\*Real\*\*.



\## Project Overview



Fake news can spread rapidly through online platforms, making it difficult to distinguish reliable information from misleading content.



This project develops and compares multiple Natural Language Processing and machine learning approaches for automatic fake news detection.



The implemented models include:



\- Logistic Regression

\- Naive Bayes

\- LSTM

\- GRU

\- BERT



The project covers text preprocessing, feature representation, model training, evaluation, and comparison using accuracy and F1-score.



\## Dataset



The project uses two CSV files:



\- `Fake.csv` — Fake news articles

\- `True.csv` — Real news articles



The dataset was prepared from `Fake.csv` and `True.csv` and used for training and evaluating the implemented models.



\### Dataset Source



The dataset is available through Kaggle:



https://www.kaggle.com/datasets/farjanakabirsamanta/true-fake-news-dataset



## Project Structure

```text
fake-news-detection-nlp/
│
├── Fake.csv
├── True.csv
├── fake_news_detection.ipynb
├── README.md
└── .gitignore



Methodology



The project applies different preprocessing and text representation techniques depending on the model.



Text Preprocessing



The text data was processed using NLP preprocessing techniques including:



Text cleaning

Tokenization

Stemming

Lemmatization

TF-IDF



TF-IDF was used to represent text for the traditional machine learning models.



The TF-IDF vectorizer used a maximum of 5,000 features.



Sequence Processing



For the recurrent neural network models, the cleaned text was converted into word sequences and padded to a maximum sequence length of 200 words.



The models used an embedding layer with a vocabulary size of 5,000 words and an embedding dimension of 128.



BERT



BERT was used as the transformer-based approach.



The project used BERT tokenization with a maximum sequence length of 128.



Models

Logistic Regression



A traditional machine learning baseline trained using TF-IDF features.



Naive Bayes



A probabilistic machine learning model trained using TF-IDF text features.



LSTM



A recurrent neural network model trained using padded word sequences.



GRU



A recurrent neural network model used to compare its performance with LSTM.



BERT



A pretrained transformer model fine-tuned for binary fake news classification.



Results

Model	Accuracy	F1-Score

BERT	99.96%	99.96%

GRU	99.84%	99.83%

Logistic Regression	98.65%	98.59%

Naive Bayes	92.66%	92.25%

LSTM	92.42%	92.61%



BERT achieved the best overall performance in this experiment, with an accuracy and F1-score of 99.96%.



BERT also produced the lowest number of incorrect predictions, with only 4 wrong predictions on the test set.



Technologies

Python

Pandas

NumPy

Scikit-learn

TensorFlow / Keras

Transformers

NLTK

Matplotlib

Seaborn

Jupyter Notebook

Project Goal



The goal of this project is to explore how different NLP and machine learning techniques can be applied to automatic fake news detection.



The project compares traditional machine learning models, recurrent neural networks, and transformer-based models to evaluate their effectiveness for text classification.



Future Work



Possible future improvements include:



Testing the models on newer and more diverse datasets

Evaluating model robustness on unseen topics and news sources

Testing additional transformer architectures

Developing a web application for real-time fake news prediction

Exploring models such as RoBERTa and other advanced transformer architectures

Academic Context



Developed as part of an AI312 – Natural Language Processing university project.

