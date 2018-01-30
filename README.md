# Project 12 Semantic Segmentation

In this project a Convolutional Neural Network (CNN) based on a VGG-16 image classifier performs semantic segmentation to identify roads in scene images. The VGG-16 is originally described in the paper "Fully Convolutional Newtorks for Semantic Segmentation" by Long, Shelhamer, and Darrell.

## Strategy

  The VGG-16 is pre-trained. The output of the pre-trained network is a 1x1 convolution layer that is used as input for the transpose layer. A 1x1 convolution of layer 4 is added. These are together run into a convolutional transpose is passed into a 1x1 of layer 3. Finally a transpose convolutional layer feeds to the output.

  An Adam optimizer is used for optimization
  
## Training

  Three training runs were done. In each, the batch is set to 5 and the kernel is initialized to stddev = 0.01 and it is regularized to 0.001. The runs were for 40 epochs, 50 epochs, and 100 epochs. Also a keep probabliity of 0.5 and a learning rate of 0.0009 are used.


## Results
  
  The losses on the 100 epoch run were:
  Epoch | Loss
  
  1    |0.254
  10   |0.078
  20   |0.042
  30   |0.025
  40   |0.034
  50   |0.022
  60   |0.030
  70   |0.021
  80   |0.108
  90   |0.017
  100  |0.012

## Images
 
  Below are sample images from each of the test runs:
   40 Epochs  | 50 Epochs | 100 Epochs
   
(./um_000001.png)|(./um_000010.png)|(./um_000012.png)



Below is the original Udacity README for this project:

# Semantic Segmentation
### Introduction
In this project, you'll label the pixels of a road in images using a Fully Convolutional Network (FCN).

### Setup
##### Frameworks and Packages
Make sure you have the following is installed:
 - [Python 3](https://www.python.org/)
 - [TensorFlow](https://www.tensorflow.org/)
 - [NumPy](http://www.numpy.org/)
 - [SciPy](https://www.scipy.org/)
##### Dataset
Download the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) from [here](http://www.cvlibs.net/download.php?file=data_road.zip).  Extract the dataset in the `data` folder.  This will create the folder `data_road` with all the training a test images.

### Start
##### Implement
Implement the code in the `main.py` module indicated by the "TODO" comments.
The comments indicated with "OPTIONAL" tag are not required to complete.
##### Run
Run the following command to run the project:
```
python main.py
```
**Note** If running this in Jupyter Notebook system messages, such as those regarding test status, may appear in the terminal rather than the notebook.

### Submission
1. Ensure you've passed all the unit tests.
2. Ensure you pass all points on [the rubric](https://review.udacity.com/#!/rubrics/989/view).
3. Submit the following in a zip file.
 - `helper.py`
 - `main.py`
 - `project_tests.py`
 - Newest inference images from `runs` folder  (**all images from the most recent run**)
 
 ## How to write a README
A well written README file can enhance your project and portfolio.  Develop your abilities to create professional README files by completing [this free course](https://www.udacity.com/course/writing-readmes--ud777).
