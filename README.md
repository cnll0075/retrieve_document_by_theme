# Retrieve Document By Theme

In this notebook, I aimed to retrieve articles from wikipages of 50 actors/actresses which describe whether he/she is socially progressive or not. 

Generally topic modelling is an unsupervised approach  where topics will only be determined by looking at keywords of each topic after algorithm has finished running. To tackle this interesting and highly practical problem to retrieve documents based on pre-defined topic, I’ve decided to take the semi-supervised approach.

For a quick (3 hours) ideation, I used a python package called GuidedLDA. GuidedLDA can have ‘seed’ key words that can help pre-determine/cluster topics containing those keywords. This way the clustering algorithm can force the model to have a head-start and put those relevant documents together. 

To get some seed words, I got the top 20 most common words from 7 wiki pages: 'LGBT social movements','Environmental movement','Human rights movement', 'Anti-war movement','Animal rights movement','Black Lives Matter', 'Civil rights movement’. These pages were selected because they have good representations of social progressiveness. 

Then these seed words were passed in GuidedLDA with a confidence of 1. After training, top 10 documents with the highest probability belonging to that pre-defined topic was returned. As can be seen from the result, the returned articles did mostly talk about political/social aspects of that actor/actress.

To do this more formally,  I would hand create labels for both positive and negative documents (or scrape pages with pre-determined labels) and build a classification model (similar to ULMFIT), where text classification was done by fine-tuning a pre-training language model (like LSTM-AWD or BERT).

Thank you for reading!

Angela Tao

 
