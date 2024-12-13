# LSTM_Next-word-Prediction

Next Word prediction based on the Deep learning model - LSTM

Steps:
Data Collection - Used the Shakespeare's "Hamlet" as dataset.

Data pre-processing - Text data is tokenized, converted into sequences, padded to ensure uniform input lengths, then split into training and test sets.(Training input sequences are n_gram_sequences having varied length of inputs)
And output is One Hot Encoded based on vocab size

Model Building - An LSTM Model is built with embedding layer - vocab_size = 4818,dim = 100,input_len = len of max input seq(14), 2 LSTM Layers, a dense output layer with softmax activation function(with no of neurons = vocab size) to predict the probability of the next word.

Model Training- MOdel is trained using prepared sequences with early stopping implemented to prevent overfitting.Early stopping monitors the validation loss and stops training when the loss stops improving.

Model Evaluation - Evaluated using a set of example sentences to test its ability to predict the next word accurately.

Deployment: Streamlit Web Application to allow users to input a sequence of words and get the predicted next word in real-time.
