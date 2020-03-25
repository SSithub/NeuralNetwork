# Neural Network Class/Library For Java

An adjustable neural network class or library, with an example of solving the XOR problem along with a classification variation.

Thought it would be easier to have the necessities of neural networks in one class. I add features when I need to use them in my other projects.

I could not think of another way to display a graph in JavaFX of the progress of the network, so I settled on a outer class that nests the neural network class inside.

See the XOR example for an example on initializing a neural network: https://github.com/SSithub/Neural-Network-Library-Class/blob/Floats/src/neuralnetwork/XOR.java

To show a graph of the cost or accuracy can be shown with the static method NNLib.graph(boolean, NN), where true will measure accuracy while false will measure cost. The NN argument takes in the neural network that will be used to plot the graph. There can only be one neural network that can be graphed currently, as there can not be more than one JavaFX thread.

NNLib.graphJFX(boolean, NN) should be used when working with JavaFX applications. It will create a new stage instead of creating a new JavaFX thread to avoid the exception that comes with multiple JavaFX threads. The second argument takes in the neural network that will be graphed. This version of the method allows for graphs of different neural networks.

The parameters take in enums from the NNLib class:

    public enum LossFunction {
        QUADRATIC, CROSS_ENTROPY
    }

    public enum ActivationFunction {
        SIGMOID, TANH, RELU, LEAKYRELU, LINEAR, SOFTMAX
    }

    public enum Optimizer {
        VANILLA, MOMENTUM, ADAM, NADAM
    }

    public enum Initializer {
        VANILLA, HE, XAVIER
    }
