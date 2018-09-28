# An Algorithm for a Dog Breed Identification App

## Overview
This project is based on template code and guidance provided by Udacity as part of the Machine Learning Engineering Nanodegree. The work is done on a Jupyter notebook, using Python3. 

## Brief Description
I work with two datasets. The dataset of dog images contains 8351 images in 133 dog categories. This set is split into a 6680 images training set, a validation set with 835 images and a test set with 836 images. The second dataset contains 13233 human images. 

First, I use OpenCV implementation of Haar cascade classifier to detect human faces in images. This is achieved with a pre-trained face detector available on github.

Next I use a pre-trained ResNet-50 model to detect dogs in images. The weights of this CNN were pre-trained on ImageNet, a very large dataset used for image classification and other vision tasks. This is performed in Keras. 

Next, I create a CNN that consists of several groups of convolutional layers, batch normalization layers and maxpooling layers, the final layers are a global averge pooling layer and a dense layer. I use a RMSprop optimizer and ran the algorihm on 10 epochs to obtain a 23.44% accuracy.  

Comparing to a pre-trained VGG-16 model provided by Udacity, I create a CNN that identifies dog breeds and uses a pre-trained Xception model. After a run on 20 epochs this model reaches an accuracy of 85.17%. Finally, I applied the model to predict the dog breeds for several new images. I also combine these results with results of the human face detector to determine which dog breed a human resembles the  most.
