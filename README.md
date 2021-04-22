# Sentiment Analysis on Covid-19 tweets

Sentiment Analysis is an analysis of the sentence, text at the document that gives us the opinion of the sentence/text. In this project, we haveimplemented a model which inputs a sentence and predicts the sentiment of the sentence. The main objective of this project is find the sentiment of the tweet using Deep Neural Network Architecture.  

## Approach 

 Recurrent neural network (RNN) is a type of deep learning model that is mostly used for analysis of sequential data. But it faces issues like vanishing gradient.So LSTMs were developed to deal with the vanishing gradient problem that can be encountered when training traditional RNNs. So in our notebook we have implemented two approach.

1. <b>Long short-term memory</b>(LSTM): units are units of a recurrent neural network (RNN). An RNN composed of LSTM units is often called an LSTM network. A common LSTM unit is composed of a cell, an input gate, an output gate and a forget gate. The cell remembers values over arbitrary time intervals and the three gates regulate the flow of information into and out of the cell.

2. <b>BidirectionalLong short-term memory</b>(BiLSTM) are really just putting two independent RNNs together. This structure allows the networks to have both backward and forward information about the sequence at every time step. Using bidirectional will run your inputs in two ways, one from past to future and one from future to past and what differs this approach from unidirectional is that in the LSTM that runs backward you preserve information from the future and using the two hidden states combined you are able in any point in time to preserve information from both past and future.

### Prerequisites

One can try this in google colab, need to install some libraries such tensorflow.keras,numpy,pandas etc. We have implemented the Deep Learning model using Keras library.

### Implemntation

#### Preprocessing
 <b>Preparing the text for deep learning model using Tensorflow2
  * Removal of stop words
  * Tokenization 
  * Sequencing
  * Padding
  
Accuracy is one metric used for evaluating classification of tweets into positive, negative and neutral tweets.

Using LSTM model, we have 6 layers. One LSTM layer, two Dense layer, one input layer, one embedding layer and one global max pool layer.
The validation accuracy is around 65%.

Using BiLSTM model , we have used 10 layers. Out of that we have used 3 stacked BiLSTM layers, 2 Layers for Batch normalization, one embedding layer, and three dense layers.
The validation accuracy is 97%.

