
*I find the concept of embeddings to be one of the most fascinating ideas in machine learning. If you’ve ever used Siri, Google Assistant, Alexa, Google Translate, or even smartphone keyboard with next-word prediction, then chances are you’ve benefitted from this idea that has become central to Natural Language Processing models. There has been quite a development over the last couple of decades in using embeddings for neural models (Recent developments include contextualized embedding techniques leading to cutting-edge models like BERT and GPT2).*

### Universal Sentence Encoder (https://arxiv.org/abs/1803.11175) with its implementation through Tensorflow (https://tfhub.dev/google/universal-sentence-encoder/2) has come through clutch in getting the most ordinally out of sentences as a whole instead of looking at it as just a group of words. This ability to semantically draw value out of textual data, makes it a great candidate for **Opinion Mining**.


### This project attempts to use Universal Sentence Encoder to embed tweets and classify them into positive VS negative.
#### I tried to measure classification performance across sentence VS work embedding techniques for sentiment analysis.

## Instructions to Run
### **Install docker**
https://docs.docker.com/engine/install/

### Clone this repo
```bash
cd /some/dir
git clone https://github.com/advaithsrao/TwitterSentimentAnalysis_using_UniversalSentenceEncoder.git
```

### Pull tensorflow-1.15-gpu image from **https://hub.docker.com/r/tensorflow/tensorflow/tags?page=8&ordering=last_updated**
```bash
docker pull tensorflow/tensorflow:1.15.4-gpu-py3-jupyter
```

Get the IMAGE_ID corresponding to *REPOSITORY* tensorflow/tensorflow
```bash
docker images
```

Copy this IMAGE_ID

### Spin up the container
```bash
docker run -it -p 8888:8888  -v TwitterSentimentAnalysis_using_UniversalSentenceEncoder:/tf <IMAGE_ID>
```

#### Please open jupyter notebook throgh the link echoed on the CLI

#### Open the mail.ipynb file and you are good to run the notebook

## About the dataset

### We use the sentiment140 dataset. It contains 1,600,000 tweets extracted using the twitter api . The tweets have been annotated (0 = negative, 4 = positive) and they can be used to detect sentiment .

Content

target: the polarity of the tweet (0 = negative,4 = positive)

ids: The id of the tweet

date: the date of the tweet

flag: The query. If there is no query, then this value is NO_QUERY.

user: the user that tweeted

text: the text of the tweet

>Go, A., Bhayani, R. and Huang, L., 2009. Twitter sentiment classification using distant supervision. CS224N Project Report, Stanford, 1(2009), p.12.

