# Fake News Detection

This GitHub repository is code base for the paper 'Detecting Fake News using Siamese BERT Network'. The paper explores the possibilties of classifying news statements. We have experimented using LSTM, Bidirectional LSTM and BERT models. The Dataset used in this paper is introduced in "Liar, Liar Pants on Fire" paper and is an open-source dataset.

### LSTM Model

The LSTM Model uses news-statment which are fed into the network as tokens which are padded to a maximum length. The model is trained to 30 epochs with 'Adam' optimizer and 'BinaryCrossentropy' loss function. The model uses Keras and TensorFlow framework for training.

### Bidirectional LSTM

The architecture of Bidirectional LSTM Model is similar to the LSTM Model.

### Simple BERT Model

The Simple BERT Model uses news-statements which are fed into the BERT network. The news-statements are tokenized, converted into ids and padded to a maximum length. The resulted tensors are converted into a dataloader which is fed into a BERT model for classification. The model is trained for 5 epochs with 'Adam' optimizer and 'CrossEntropyLoss' function in PyTorch.

### BERT with Metadata (Siamese BERT Architecture)

BERT with Metadata uses news-statements and metadata (The metadata includes - subjects, speakers, jobs, states and affiliations). Both the features (news statements and metadata) are subjected to tokenization, conversion to ids and padding to a maximum length. The resulted tensors are introduced into two seperate BERT models. The results from the BERT models are concatenated with credits and used for classification. The model is trained for 5 epochs with 'Adam' optimizer and 'CrossEntropyLoss' function in PyTorch.

![BERT with Metadata](/images/bert_with_metadata.png)

### Final BERT Model (Siamese BERT Architecture)

The Final BERT Model uses news-statements, metadata, true words, and false words. All the features are subjected to tokenization, conversion to ids and padding to a maximum length. The resulted tensors are introduced into seperate BERT models. The results from the BERT models are concatenated with credits and used for classification. The model is trained for 5 epochs with 'Adam' optimizer and 'CrossEntropyLoss' function in PyTorch.

![Final BERT Model](/images/Final_BERT_Model.png)
