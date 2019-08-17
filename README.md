## Overview

This is a project where I use Pytorch to buld and train a CNN model to predict if a picture of a face is `dark`, `light` or `ok`. 

**Goals of this Project:**

* Develop a pipeline for generating dataset.
* Develop a network in Pytorch that predicts light condition of an image.
* Describe the result

**NOTE:** Create the environment from the `environment.yml` file: `conda env create -f environment.yml`

---
## Dataset

Overall steps for developing dataset:
- download the data: video files of three categories ('dark', 'light', 'ok')
- create virtual environment
- expolre data
- decide on the data format for training
- extract images of faces from videos
- split data to training and validation parts

## CNN Model

Overall steps for developing a classification model:
- choose simple model (for ex. LeNet)
- define custom Dataset class and needed transformations (resize, normalize e.t.c.)
- try to overfit on a small dataset
- tune hyperparameters
- use the whole dataset for training
- check inference

## Results

- Explored different face detectors such as opencv's detector based on Haar Cascades, dlib's HOG and CNN based face detectors
- Trained a classifier using LeNet architecture to classify images of faces ('dark', 'light', 'ok')
- Achieved overall accuracy of 94,12 % on validation set

## Reflection

The task was a two-part project. First, I needed to pick the right tool for face extraction from images. Second, I have trained a simple convolutional neural network for classification.

By default I assumed that as an input for the model there always would be images with faces. However, in order to make more robust classificator it would be a good thing to add (as a first stage) a check procedure for face/not face.

Also, having more training data would lead to a better performance of a CNN model.

