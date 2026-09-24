# Micrograd, reimplemented

A reimplementation of Andrej Karpathy's
[micrograd](https://github.com/karpathy/micrograd): a scalar autograd engine and a small neural network library on top of it, written without any framework.

## Components
- `Value`: an object that wraps a number and "remembers" the operations that produced it, allowing the computation of its gradient through backpropagation.

- `Neuron`, `Layer`, `MLP`: a full multilayer perceptron with tanh activations. 

- A gradient descent training loop on a very small dataset of four points. 

## Result
A 3-4-4-1 network trained for 100 steps (learning rate 0.05) on four points with targets 1, -1, 1, -1.

The weights are initialised randomly, so every run outputs a different prediction and final loss. In the run saved in the notebook, the loss falls from 2.75 to 0.006 and the predictions are:

| Target | Prediction |
|-------:|-----------:|
|    1.0 |      0.945 |
|   -1.0 |     -0.977 |
|    1.0 |      0.971 |
|   -1.0 |     -0.958 |