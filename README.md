# ImageClassifier-DogvsCat-
This repository covers a Image Classifier using VGG16 model and a traditional Multi-layers CNN

Develop a Deep Convolutional Neural Network Step-by-Step to Classify Photographs of Dogs and Cats
The Dogs vs. Cats dataset is a standard computer vision dataset that involves classifying photos as either containing a dog or cat.

Although the problem sounds simple, it was only effectively addressed in the last few years using deep learning convolutional neural networks. While the dataset is effectively solved, it can be used as the basis for learning and practicing how to develop, evaluate, and use convolutional deep learning neural networks for image classification .

# Data Source
This project is basically a training tutorial from Kaggle competition.
Pictures of cats and dogs can be collected using following link: https://www.kaggle.com/c/dogs-vs-cats/data
This project is composed of 12500 pictures of dog and 12500 pictures of cat.

# Modeling and Methods
This project contains two possible Deep Learning Method: traditional Multi_layers CNN and a Fine-tued VGG16 Model
Data Preprocessing: 25000 pictures are split into Traning dataset, Validation dataset and Testing dataset using OS library in Python; convering 1000 of Traning dataset, 200 Validation dataset and 1000 Testing dataset. Considering the capability of my computer and running time, sampling data is scaled to this size.Datasets are using VGG16 preprocessing with augmentation to prevent overfitting problem, letting pictures flip, zoom and shear. 

The first traditional Multi- layers CNN is using 2 convenlutional layers, 2 maxpooling layers, 1 fully-connect layer and 1 output layer
The Second VGG16 Model is using non-trainable parameters for all layers except the last output layer to reduce the running time for adjusting weights.
Additionally, these two models are both utilizing Callbacks(earlystopping, ReduceLROnPlateau, and also batchnormaliztion. The dropout layers rate is set to 20%.

# Result 
roc_auc_score of Multi-layers CNN is 0.7345
roc_auc_score of Fine-tuned VGG16 is 0.9749
