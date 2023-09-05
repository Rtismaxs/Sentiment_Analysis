# Sentiment_Analysis
This repository represents the work achieved for my thesis concerning the sentiment analysis of customers reviews.

This thesis is composed of three notebooks. Each notebook achieves a specific task. The data used for the purpose of this thesis is open data. In fact, we can find this data online:
'https://www.kaggle.com/datasets/bittlingmayer/amazonreviews?datasetId=1305&sortBy=voteCount&select=test.ft.txt.bz2'
There are two datasets: 'train.ft.txt.bz2' and 'test.ft.txt.bz2'. In this thesis, we only use the 'train.ft.txt.bz2' which contains a total of 3.6 million reviews. This data is used as the input of the notebook 'PreProcess_Data_Thesis.ipynb'.

Indeed, this notebook is responsible of the pre-processing applied on the raw data 'train.ft.txt.bz2'. The notebook is structured around the multiple transformations performed. The running of this notebook can take some time as we deal with a lot of reviews. At the end of this notebook, we generate the csv file 'small_data_preprocessed.csv'. This output is then used for the notebook 'Machine_Learning_Thesis.ipynb'.

In fact, the notebook starts with the csv file 'small_data_preprocessed.csv' for the training of several machine learning algorithms. The running of the notebook can be achieved on CPU and take a lot of time as we train several algorithms (Random Forest and SVM with different words embeddings). For the GloVe word embedding, we need to load the txt file 'glove.twitter.27B.100d.txt'. For the other words embeddings, we don't need other inputs. This notebook doesn't have any outputs except metrics scores from the Machine Learning models.

Finally, we have the notebook 'Deep_Learning_Thesis.ipynb' which is the training of several BERT versions. This notebook needs to be process on GPU and also has as input the csv file 'small_data_preprocessed.csv'. The running of this notebook also takes a long time as we fine-tune Deep Learning models on a large amount of data.
