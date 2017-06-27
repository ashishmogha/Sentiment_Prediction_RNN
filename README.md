# Sentiment_Prediction_RNN

The problem of `sentiment classification` has received a lot of attention of late
* It finds applications in the fields of business intelligence, recommender systems (so as to be able to understand the
sentiment in a user’s feedback), in online surveys that have `natural language sentences` as responses,
message filtering, assessing movie review polarity, among others.

* Here I have implemented a  **recurrent neural network(RNN)** that performs **sentiment analysis**.



# Architecture 

![screenshot capture - 2017-06-16 - 03-19-29](https://user-images.githubusercontent.com/17912055/27203280-b4c43a24-5242-11e7-9662-df0f70144951.png)

* Pass in words to an **embedding layer**.Need an **embedding layer** because there are tens of thousands of words, therefore need a more efficient representation for our input data than **one-hot encoded vectors**

* From the **embedding layer**, the new representations will be passed to **LSTM** cellls. These will add recurrent connections to the network so we can include information about the sequence of words in the data.

* Finally, the **LSTM** cells will go to a sigmoid output layer here. We're using the `sigmoid` because we're trying to predict if this text has positive or negative sentiment. 

* The output layer will just be a single unit then, with a `sigmoid` activation function.

* Don't care about the `sigmoid` outputs except for the very last one,ignore the rest.Calculate the cost from the output of the last step and the training label.



# Dataset

* Here I have used a  dataset of movie reviews, accompanied by labels.
1. [reviews.txt](https://raw.githubusercontent.com/ashishmogha/Sentiment_Prediction_RNN/master/reviews.txt)
2. [labels.txt](https://raw.githubusercontent.com/ashishmogha/Sentiment_Prediction_RNN/master/labels.txt)


# Requirements

1. Tensorflow
2. Numpy 




