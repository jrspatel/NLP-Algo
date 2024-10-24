# NLP-Algorithms 

All the SOTA models are pre-trained on large amounts of data usually [ 4.5 gb (GPT-1) to 100 gb ] and then fine-tuned on task specific data. The larger the Language Model, the better the performance or result.

## GPT 1
- GPT1 uses transformer decoder architecture with 117M parameters.

- 12 transformer blocks with 12 multi head attention, the size of the hidden layer being 768
   i.e.,d-model = 768, d-k = 64. 

- Used Learned position embeddings instead of sinusoidal version (cos, sin function to keep track of the order of the input sequence ). Learned positional embeddings can be trained in a neural network. Even thhough the word seq is fixed, the transformer
  process the whole input seq at once and they need to understand the relative positions of the words sometimes not just the absolute.

- GPT replaced ReLu activation with **GELU { Gaussian Error Linear Unit }** which has the properties of ReLU, dropout and zoneout.
   ReLU has a problem with dead neurons [ either 0,1 ] 
    GELU formulae : ___________________ 

- The Tokenization technique used here is  **BPE ( Byte-Pair Encoding )**
-  BPE Rules for Training and Inference
    -  Traning
    -  Inference 

**Zero-Shot behaviour** 
- using the pre-trained model to perform tasks without fine-tuning.
  e.g., for sentiment analysis append "very" to every example and limit the output distribution to "positive" and "negative".
   

## GPT 2 

- It follows a similar architecture to GPT 1, with more parameters increased from (117M to 1.5B, with 4 variants) and trained on a 40GB text size.

- Treats all NLP tasks as word prediction tasks

- Architectural modifications compared to GPT 1
    - used pre-layer normalization instead of post-layer normalization allowing to use larger leraning rates.
    - Context size increased from 512 to 1024 tokens.
    A modified Initialization of parameters is used to stabilize the gradients during training. The weights are scaled by a factor of 1/root(N), and 'N' is a number of layers.
    - GPT 2, uses **byte level BPE (BBPE)** , allows the model to represent any text encoded in UTF-8 and also **text from different languages and special characters**.


 ## GPT 3 

 - Scaled to more parameters 175B and trained on extensive dataset of 300B tokens.

 - Introduced the concept if **In-context learning (ICL)**, enables the model to learn from the prompt's contents.

## BERT (Bidirectional Encoder Representation from Transformers) 

- Encoder only Architecture

- **Input** to the bert is parsed with special tokens [SEP] & [CLS]. These separators distinguish the sentences, so in-addition with the tokens, positional embeddings bert also receives segment embeddings.
- 

- 

- 
 
  
- 

