# Master Thesis NN infrastructure
Code used to test different types of Neural Network to infer local Ocean Current forecasts (Code of the simulator not included).

Note: The data used to train and evaluate the models is voluntarily not included.

## Types of Neural Networks evaluated:
+ Multi-Layer Perceptron
+ Convolutional Neural Networks:
    + 2D U-Nets
    + **3D U-Nets**
+ Recurrent Neural networks:
    + RNN
    + LSTM
    + GRU
+ ConvLSTM
+ 2D U-Net-LSTM

All the models (including the GP) are located in the folder: *ocean_navigation_simulator/ocean_observer/models/*
The file *ocean_navigation_simulator/ocean_observer/Observer.py* is used to use the GP and the NN to have improved Ocean Current forecasts.

The models were first trained and evaluated without any grid search optimization but, instead, by manually testing some set of hyperparameters.
The process to test each type of architecture was to 1)Overfit on a small dataset 2) Increase the dataset progressively and try to generalize.
I followed more or less the recipe from: [Andrej Karpathy's blog post](http://karpathy.github.io/2019/04/25/recipe/).

An ablation study was then done focusing on a) the Gaussian Process, b) the 3D U-Net & c)the GP+3D U-Net.

The Master Thesis is available [here](https://www.research-collection.ethz.ch/handle/20.500.11850/589232).

If you have any question, please reach out to killian.kaempf[at]gmail.com
