# Sentiment Analysis using BERT

Sentiments analysis of tweets related to psychiatry and medicine-related scientific articles.

## Objectives

The objectives are:
1. To collect the tweets meant for sharing reviews about various research-related work in medicine domain and labelling the same.
2. To Build classifier models using BERT algorithm with two different approaches and comparing the results of both approaches.
3. To predict the sentiment of tweets using the best approach and analyzing the results.
4. To investigate and share areas in which there is scope of further improvement.

## Approach

To achieve the objective, two variations of sentiment classifiers using BERT(Bidirectional Encoder Representations from Transformers), the state-of-the-art method are built. One is a generic classifier masking the article name in the tweet and another is a target-based classifier masking the article name in the tweet as well as giving the article name as a target towards which sentiment will be identified.

## Dataset

I have extracted the data from https://explorer.altmetric.com using beautiful soup library. 

## Results

I have tried two approaches using the BERT model to classify the sentiment of a tweet. In the first approach, I have masked the Article name in the tweet and used it in the BERT input, and in approach two, in addition to masking, I have used Article Title as an aspect and given as a second sentence to the BERT input. After many trials of fine-tuning, I found that the model using approach two is performing better. I compared the results of BERT based model with machine learning approaches carried out previously in the same area (https://link.springer.com/chapter/10.1007/978-3-030-34058-2_29).  BERT based model with an accuracy of 93.5% and Weighted F1 score of 93% outperforms the machine learning model SVM whose accuracy is 91.6% and F1 score 91%.
