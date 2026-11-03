# Sentiment Analysis

This project was completed as a requirement for a Udacity Nanodegree program. It builds on the provided SentimentScope starter notebook, with completed code for sentiment classification and a shortened presentation for GitHub.

## Project Overview

Movie reviews offer insight into how audiences feel about a film. This project explores how a transformer model can learn to recognize that sentiment and classify a review as positive or negative.

Using the IMDB movie review dataset, I worked through the process of preparing text data, building a transformer classifier with PyTorch, and training it to make predictions on unseen reviews. The goal was to achieve more than 75% test accuracy.

## Main Components

- **Data preparation:** Loading positive and negative reviews, exploring the dataset, and separating the training data into training and validation sets.
- **Tokenization and data loading:** Converting reviews into token IDs with the `bert-base-uncased` tokenizer and using PyTorch datasets and data loaders to prepare batches.
- **Transformer architecture:** Bringing together attention heads, feed-forward layers, and transformer blocks, then adding a classification layer to predict sentiment. The model is trained from scratch.
- **Training and validation:** Training the model with cross-entropy loss and AdamW, while checking validation accuracy after each epoch.
- **Testing and evaluation:** Evaluating the trained model on the held-out test set to see how well it classifies reviews it has not seen during training.

## Results

After three epochs, the model achieved the following recorded results:

| Evaluation | Accuracy |
|---|---:|
| Validation before training | 50.92% |
| Validation after training | 76.76% |
| Test after training | 76.61% |

The test accuracy exceeded the project's 75% target. The improvement from the untrained baseline shows how training helped the model learn patterns associated with positive and negative reviews.

## Tools and Dataset

The project uses Python, PyTorch, pandas, NumPy, and Hugging Face Transformers. Reviews come from the [IMDB Large Movie Review Dataset](https://ai.stanford.edu/~amaas/data/sentiment/).

