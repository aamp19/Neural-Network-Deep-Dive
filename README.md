# Neural-Network-Deep-Dive
Neural networks are made up of layers of neurons. Neurons are the core processing units of 
the neural network. Layers include: input layer, hidden layers, and output layer. The input 
layer receives the input of the dataset. The hiddens layers are where most of the computation 
that is required by the network. The output layer simply predicts the final output. Neurons of one 
layer are connected with neurons of the next layer through channels. These channels are associated with 
numerical values known as weight. The inputs are multiplied with the corresponding weight, and the sum is 
sent as input to the hidden layer neuron. The neurons of the hidden layer are associated with a numerical 
value known as the bias, and is added to the input sum. Then the current sum is passed through another function, 
called the Activation Function. The Activation Function determines if a particular neuron will get 
activated or not. The activated neurons transmits its data the neurons in the next layer. The process of sending sums of neurons the next layers of neurons is known as forward propagation. 
In the output layer, the neuron containing the largest value goes on, and determines the output. The determined output is a predicted output. 
The data that is provided contains the actual output. There will be a comparison with both the predicted, and actual output. 
If the predicted output is different from the actual output, the information will be used to train the neural network, by looking at the magnitude of error. 
This information is transferred backwards into the network, which is known as backpropagation. Based off of the magnitude of error in the backprogation, the weights will then be adjusted. 
Backprogation is iteratively performed with multiple inputs. This process will go on until, the weights are adjusted correctly so the predicted outcome matches the actual outcome. 

For the problem being solved,

The classes used for this problem include: DataProcessor, and NeuralNetwork.

In the DataProcessor class, the data is brought into the program. The gender column and labels are then one hot encoded. 
The data input and output values are identified, and split up. Once the inputs and outputs of the 
data are separated, the input is then feature scaled, and is returned in the scaler function. 
In the datasets function, the inputs and outputs are split into training (70%) and test (30%) sets. 
There is a sigmoid function that will simply sigmoid the predicted outcome. The softmax function computes softmax values 
for each sets of scores in the input. In the softmax_derivative function, the softmax derivative of the inputs are calculated, stored, and displayed in a list. 

In the NeuralNetwork class, epochs (amount of iteration for trained data), and alpha (used for updating weights) are initialized. 
Weights and biases are initiazlised with empty lists. Random values are set for weights and biases at each layer. Empty lists and dictionaries made to store errors and outputs. 
The train function is used to train the input and output data so backpropagation can take place for the weights to be accurately updated. 
The process of forward propagation will take place over how ever many epochs there are. The average cross entropy error for each epoch is stored in a list that was initialized in the __init__. 
Derivatives with respect to each weight and bias are initilized. The derivative of the Loss function with respect to activations, z, weights, and biases of each layer takes place.
The derivatives sum over each softmax partial derivative.The weights and biases are updated due to backpropagation.
The sum of derivatives over every softmax partial derivative derivative occurs. The weights and biases are updated appropriately. 
