# Next-Frame-Video-Prediction-using-convolutional-LSTM

## Dataset: Moving MNIST

## Overview 
- In the project we predict next-frame f_(n+1), our model will be using a previous frame f_n. 
- To make the predictions our model will need "shifted" inputs and outputs, Say input data is frame x_n, which is used to predict frame y_(n+1) 
- Our data consists of sequences of frames, each of which are used to predict the upcoming frame. We plot each of the sequential image for one random data example.
![image](https://user-images.githubusercontent.com/109361931/229404696-81f6097b-b7d6-4e89-b824-0cece01baff4.png)

- To build a convolutional LSTM model, we construct 3 `ConvLSTM2D` layers with batch normalization, followed by a `Conv3D` layer for the spatiotemporal(both space and time information) outputs. We accept the inputs of shape #(batch_size, num_frames, width, height, channels)

- Model Compilation: 
  - Loss function used: binary_crossentropy
  - Optimizer used: Adam
  
- Model Training: 
  - 
