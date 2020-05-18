# Keras---MNIST---CNN--- Accuracy 99.95%
A simple Convolution Neural Network trained on the famous MNIST dataset that touched an accuracy of 99.95%.
Although the accuracy of the final epoch is 99.82%, the CNN model achieved an accuracy of 99.95% in the 2nd last epoch which indicates that the model performed pretty well on the dataset.

This is an extremely simple model without any special layer or function like Dropout, Data Agumentation, Early Stopping etc.
Based on experiments for no.of epochs between 20 and 30 the model achieved this accuracy.
The model consists of the following layers/components:
1. It as has 3 Convolutional layers with 
  a. 32 ,64 and 64 filters respectively 
  b. activation function ->'relu' (for all the layers) 
  c. different 'kernel_size'.
2. After the 3 Convolutional layers there are 2 MaxPooling2D layers with the same 'pool_size'.
3. After the MaxPooling2D layers comes the Flatten layer.
4. Finally comes a fully connected Dense layer with 128 neurons and then the output layer with 10 neuron corresponding to the no.of features in the dataset ( i.e. digits 0 to 9 ) with activation functions as 'relu' and 'softmax' respectively.

The summary of the model is as follow: 
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   

=================================================================
conv2d (Conv2D)              (None, 25, 25, 32)        544       
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 23, 23, 64)        18496     
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 22, 22, 64)        16448     
_________________________________________________________________
max_pooling2d (MaxPooling2D) (None, 11, 11, 64)        0         
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 5, 5, 64)          0         
_________________________________________________________________
flatten (Flatten)            (None, 1600)              0         
_________________________________________________________________
dense (Dense)                (None, 128)               204928    
_________________________________________________________________
dense_1 (Dense)              (None, 10)                1290  

=================================================================

Total params: 241,706
Trainable params: 241,706
Non-trainable params: 0
_________________________________________________________________


