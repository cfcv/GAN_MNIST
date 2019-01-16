# GAN_MNIST
## Requirements
The basic requirements to run this project is to have installed:
Python 3, jupyter notebook, Tensorflow and Numpy.
 
## Description
This project was divided in 6 main steps:
* 1: Reading the MNIST dataset
* 2: Building inputs to the Networks
* 3: Building the Generator Network 
* 4: Building the Discriminator Network
* 5: Putting all together
* 6: Training
* 7: Viewing Results

#### Reading the MNIST dataset
In this part we load the MNIST dataset provided by tensorflow.

#### Building inputs to the Networks
Here i make a function to build the placeholder inputs of the generator and discriminator
networks. 

#### Building the Generator Network
In this part is defined a function that creates the generator network. It has two layers of n_units and 2*n_units respectively, with leaky relu activation and finally an output layer with tanh activation. It is defined with a generator variable scope so we can pass only the generator train variables for the optimizer.

#### Building the Discriminator Network
In this part is defined a function that creates the discriminator network. It has two layers of n_units and 2*n_units respectively, with a leakly relu activation and an output layer with sigmoid activation. It is defined with a discriminator variable scope so we can pass only the discriminator train variables for the optmizer.

#### Putting all together
Here i'm defining all the hyperparameters and using it to call the functions i've created to build the inputs, generator and two discriminators(one for the real data and another for the fake data). I'm defining also the losses and the optimizers.

#### Training
In this part i'm training both networks with 200 epochs and in each epoch i append the losses and some samples of the generator for looking in the future.

#### Viewing results
Here the training losses of every epoch and some samples of the last training epoch are plotted. Below we can see the evolution of the generator images throught the epochs and some sampling from it.


![alt text](https://github.com/cfcv/GAN_MNIST/blob/master/photos/evolution_gan_mnist.png)

**Sampling:**  
![alt text](https://github.com/cfcv/GAN_MNIST/blob/master/photos/result_GAN_MNIST.png)

