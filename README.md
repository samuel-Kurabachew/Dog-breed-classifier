# Dog-breed-classifier
Project done for Udacity Deep Learning Nanodegree 

In this repo we find two implementation of dog-breed classifier:
 - A classifier implemented from scratch
 - A classifier with transfer learning

## Transfer Learning: 
Transfer learning is a machine learning method where a model developed for a task is reused as the starting point for a model on a second task.
It is a popular approach in deep learning where pre-trained models are used as the starting point on computer vision and natural language processing 
tasks given the vast compute and time resources required to develop neural network models on these problems and from the huge jumps in skill that they 
provide on related problems.

In there are many approaches to apply transfer learning. In my case I used the convolutional and pooling layers in a pre-trained network [Resnet](https://pytorch.org/hub/pytorch_vision_resnet/)
from list of [Models](https://pytorch.org/docs/stable/torchvision/models.html) as a feature extractor that identifies shape and color based feature in the dataset. Then After the images has passed 
through this pre-trained feature extractor we can add one or more linear layers at the end which will act as a final classifier.

As seen from the notebook the classifier implemented from scratch have an accuracy of 11% with 20 epoches (full training cycle). But with transfer learning running for 5 epoches, we can get as high as 69% score. 
This accuracy can be better and reach upto 90 - 99% if trained for more cycles.
