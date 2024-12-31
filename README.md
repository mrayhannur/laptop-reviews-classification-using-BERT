# Sentiment and Aspect Text Classification with BERT (LAPTOP REVIEWS CASE STUDY)

## Background
A little bit of background about this project, my interest in natural language processing (NLP) and the transformative capabilities of Transformer models. Utilizing a dataset sourced from Kaggle, I aim to explore how BERT (Bidirectional Encoder Representations from Transformers) can be leveraged to accurately classify sentiments and identify specific aspects within laptop reviews. This project not only enhances my understanding of NLP techniques but also demonstrates the practical application of BERT in extracting nuanced insights from textual data.

## What is in my project
This project consist of 4 parts:
1) Exploration of Dataset and Data Preprocessing
2) Fine-Tuning BERT to Sentiment/Polarity Classification
3) Fine-Tuning BERT to Aspect Classification
4) Prediction New Data using the Fine-Tuned Model

## Dataset
The dataset is from [here](https://www.kaggle.com/datasets/charitarth/semeval-2014-task-4-aspectbasedsentimentanalysis). I use three columns from the "train" set:
1. Sentence: This column contains individual laptop review texts
2. Aspect Term: This column identifies specific features or components of laptops mentioned in the reviews.
3. Polarity: This column indicates the sentiment expressed towards the aspect term (positive, negative, neutral, or conflict).

## Result
1. Exploration and Preprocessing: I did a little exploration of the existing dataset by finding insights such as the number of rows of data, distribution of data based on polarity and aspect terms, and created a wordcloud of the most reviewed aspect terms. Preprocessing was carried out by deleting duplicate rows, dropping rows with 'conflict' polarity because their contents were too diverse, mapping aspect terms (from 700 to 16 aspects only) to make classification simpler, and did the standard text normalization. The imbalanced data is also handled using oversampling techniques.
2. Fine-Tuning BERT to Sentiment/Polarity Classification: After spliting the data, I fine-tuned the BERT model for the first case, polarity classification. By using the Confusion Matrix as an evaluation, the model performance shows good performance with an **accuracy level of 89%** for 3 class (positive, neutral, negative) classification.
3. Fine-Tuning BERT to Aspect Classification: After spliting the data, I fine-tuned the BERT model for the second case, aspect classification. By also using the Confusion Matrix as an evaluation, the model performance shows good performance with an **accuracy level of up to 90%** for classifying **16 classes**.
4. Prediction New Data using the Fine-Tuned Model: By using the same 10 rows of new data, both fine-tuned models also be able to classify sentiment classes and aspects contained in reviews.

## Things Can Be Improved
1. Exploration with Indonesian datasets and transformer models (for my relevance)
2. Directly perform multilabel classification.
3. Try to get to the deployment stage.
