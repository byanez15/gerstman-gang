# gerstman-gang
Dr. Gerstman NN research models

Neural Networks created on colab using PyTorch package

========================================
SLP: Single Layer Perceptron Class
========================================
Colab file containing the Neural_Network 
class.

Single Layer Perceptron used to analyze
MNIST hand-written digits and determine
what digit it is.

The code contains all miscellaneous 
methods used within our research. 

Training loop decides to run based on 
a chosen criterion: Accuracy OR Loss

Example initialization: 
model = Neural_Network(batch_size, learning_rate)
train(model, suppressLog: boolean, CUDA: boolean, percentage: int, criterion: String, stop_epoch: int)

----Explanation of the Parameters----
Neural_Network:
batch_size => determines how much data is passed through each sub-epoch
              ex) 30,000 implies two sub-epochs in one training epoch
learning_rate => establishes the learning rate the optimization method
                 uses. Typically 1, becomes variable based off the experiment

train:
suppressLog => default = false. Determines if we store data or not

CUDA => default = false. Determines if we will run the method on the GPU or CPU

percentage => default = 0. Determines how may weight matrix elements will be held at 0,
              effectively pruning them from training. Pruning occurs from left to right,
              and row to row. 50% pruning prunes half of all columns AND rows.

criterion => default = 'CE'. Determines the criterion being used. Won't work if you don't pass 'CE' or
             'Accuracy' as an argument (NEED TO FIX)
 
stop_epoch => default = 1000. Most runs are useless for our purposes after a certain point, 
             or unnecessary for some results. This stops the model from running more than
             X epochs.
