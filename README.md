# Neural Networks An Introduction
Understanding the basics of a neural networks

## 1. What is a neural network neuron?

Within a neural network, a neuron (or perceptron) is an elementary unit of storage that along with a mathematical function that models the functioning of a biological neuron. It is one of the basic blocks of a neural network responsible for processing data.

Typically, a neuron computes the weighted average of its input, and this sum is passed through a nonlinear function, often called activation function, such as the sigmoid or tan h or ReLU. The output of the neuron can then be sent as input to the neurons of another layer, which could repeat the same computation (weighted sum of the input and transformation with activation function).


![image](https://user-images.githubusercontent.com/52544352/134753298-ecdeb7d3-067f-4903-b423-ee1ee0498d62.png) <br />
Architechture of a Single Neuron

## 2. What is the use of the learning rate?
Learning rate is a configurable hyperparameter used in the training of neural networks that has a small positive value, often in the range between 0.0 and 1.0.

The learning rate controls how quickly the model is adapted to the problem. Smaller learning rates require more training epochs given the smaller changes made to the weights each update, whereas larger learning rates result in rapid changes and require fewer training epochs.

A learning rate that is too large can cause the model to converge too quickly to a suboptimal solution, whereas a learning rate that is too small can cause the process to get stuck.

The challenge of training deep learning neural networks involves carefully selecting the learning rate. It may be the most important hyperparameter for the model.

## 3. How are weights initialized?
Each time, a neural network is initialized with a different set of weights, resulting in a different starting point for the optimization process, and potentially resulting in a different final set of weights with different performance characteristics. Weights can be initialised in a number of ways. 
1.	Zero Initialization (unsuccessful approach) - We initialize all weights to zero
2.	Random Initialization - We initializes all weights to a random value
 - a.	Random Values picked from a small range of numbers. for example, random values picked from the range [-0.3, 0.3]
 - b.	Random Values picked from a distribution like Normal distribution or Uniform distribution.
3.	Xavier initialization  -initializes the weights in your network by drawing them from a distribution with zero mean and a specific variance
4.	He-et-al initialization - Similar to Xavier initialization, with the factor multiplied by two



## 4. What is "loss" in a neural network?
Loss is a prediction error of Neural Net. The differnce between the output of the neural net and the expected output value. The method to calculate the loss is called Loss Function.
In simple words, the Loss is used to calculate the gradients. And gradients are used to update the weights of the Neural Net. This is how a Neural Net is trained.

## 5. What is the "chain rule" in gradient flow?
To minimize our cost function we continuosly change the weights and biases to get that combination of values that give us our minimum cost function. Mathematically we do that using the concept of derivatives. We cannot take complex equations as is and simply find its derivative, we break it down into smaller parts and use derivative properties to enable us to compute it easily. 

That’s when the chain rule comes into play, when we need the derivative of an expression composed of nested subexpressions.The chain rule is conceptually a divide and conquer strategy that breaks complicated expressions into subexpressions whose derivatives are easier to compute. Its power derives from the fact that we can process each simple subexpression in isolation yet still combine the intermediate results to get the correct overall result.

![image](https://user-images.githubusercontent.com/23020975/134756464-c5d421d3-5051-478c-bf15-419bb2f9ae8f.png) <br />
In its simplest form these are the step - 
1. Introduce intermediate variables for nested subexpressions and subexpressions for both binary and unary operators. This step normalizes all equations to single operators or function applications.
2. Compute derivatives of the intermediate variables with respect to their parameters.
3. Combine all derivatives of intermediate variables by multiplying them together to get the overall result.
4. Substitute intermediate variables back in if any are referenced in the derivative equation.
