# LSTM with attention - NMT from scratch
<p style='text-align: justify;'>
 This model for Neural machine Translation(english to German) was developed from scratch during my NLP specialization with DeepLearning.ai. 
I programmed the architecture of the model and its training with Trax. 
The architecture is an LSTM network encoder decoder in which the attention mechanism has been implemented.
This type of models, called seq2seq with attention, replaced the traditional Seq2Seq models, to avoid the loss of quality and fading of the information when trying to send all the information of variable length sequences in a fixed length memory context vector from the encoder to the decoder.
 
 Program the architecture of the model following the structure in the diagram below:
 ![NTM -LSTM with attention drawio](https://user-images.githubusercontent.com/76975149/154712773-aedeaa74-a77a-46d2-9a18-1f3eb299db41.png)

Subsequently, the model was trained, for which a dataset from https://opus.nlpl.eu/ was used, specifically a subset of medical texts containing translations from English to German were used.

In the decoding and sampling steps, functions were programmed to perform random sampling. With the generated samples, minimum Risk Bayes was implemented, in which each sample was compared with the other using the ROUGE score, in such a way that the sample with the highest ROUGE average is selected.
At the end of the notebook some examples of inference with the model are carried out using temperature = 0 (greedy decoding) and temperature = 0.6.</p>

![Captura](https://user-images.githubusercontent.com/76975149/154715798-d3579618-79a8-401c-8d26-252fb49521b4.PNG) 
