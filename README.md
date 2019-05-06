# TextSummarizer
Text Summarizer implementation with Tensorflow 2.0 using conditional GAN

# Introduction
Text summarizer can be used in various applications such as: quick overview of large set of text documents, search result summary for web pages, email classification/summarization... The classical example of how human summarizes text is best illustrated by the scientific papers: for a paper of 4-5 pages (around 5000 words), the owner often writes a abstract of that paper in short summary (around 250 words). Taking a large collection of scientific papers, we can develop a machine learning model that will be trained and eventually be able to generate good abstract from given text input (5000 words) the same way an author would write an abstract.

# How it works
Firstly the text input (full paper text and abstract text) need to be converted into vectors (so called embedding). There are several pre-trainned Word2Vec model. This project considered using the Glove (Global Vectors for Word Representation). The dataset for training and testing comes from the CORE dataset. The CORE dataset contains millions of research output text (full text and abstract) and it can be freely download from the (https://core.ac.uk/services/dataset/) CORE project website. Then the training data is used for a conditional GAN which has a Generator and a Discriminator. The Generator takes a training full paper text and try to generate a corresponding abstract. The Discriminator will give feedback to the Generator on real abstract and generated abstract. Over the time, the Generator will learnt and improve the generated output, make the text similar to a real abstract.

# Acknowledgement
This project would not be completed with the tutorial/data/work from sites listed below. My big thanks to the authors.

    Pix2Pix: Image to image translation using conditional GAN' https://www.tensorflow.org/alpha/tutorials/generative/pix2pix

    CORE Dataset: Millions of research output text (full text and abstract) https://core.ac.uk/services/dataset/

    GLOVE: Global Vectors for Word Representation https://nlp.stanford.edu/projects/glove/

    GloVe-as-a-TensorFlow-Embedding-Layer https://github.com/guillaume-chevalier/GloVe-as-a-TensorFlow-Embedding-Layer
