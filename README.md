# Quora-Questions-Similarity
 
 Kaggle : https://www.kaggle.com/c/quora-question-pairs
 
 Preprocessing:
     
     1. Removing html tags
     2. Removing special characters
     3. Lower the text
     
 
 Models:
 
    VOCAB_SIZE = 8000
    BATCH_SIZE = 2048
    Dense_Units = 256
    MAX_LENGTH = 64
 
    1. LSTM based Siamese Model with Feedforward Neural Network head.
    
          Trains its own word embeddings layer

    
    2. LSTM based Siamese Model with Feedforward Neural Network head with Glove embeddings, added features of questions length and number of common words
    
          Uses Glove word embeddings
          features of questions length
          feature of number of common words
    
    3. LSTM based Siamese Model with Feedforward Neural Network head with Glove embeddings, added features of questions length, number of common words and popularity of questions.
    
          Uses Glove word embeddings
          features of questions length
          feature of number of common words
          feature of question popularity in dataset (leaky features)
          used class re-weighting to train

 Evaluation:
 
     Criteria: Log-Loss
     
     Model 1:
         Private Score: 0.47721
          Public Score: 0.47593
     
     Model 2:
         Private Score: 0.30949
          Public Score: 0.30655
          
     Model 3:
         Private Score: 0.17376
          Public Score: 0.16979
     
     
          
          
        
