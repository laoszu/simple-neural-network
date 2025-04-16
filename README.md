# simple neural network
This is my first real implementation of the neural network. So much fun!

The XOR problem was chosen, because it's the simplest introduction to the MLP concept. I got the whole theory behind it from [here](docs/goodsource.pdf), where XOR was shown as the standard example of MLP implementation.

I decided to use SDL with C++, because ~~I like suffering~~ it wanted to try something new as well. ~~...Aand I got over-C-ed during my univeristy course 😊~~.

# Background
MLP (<b>m</b>ulti<b>l</b>ayer <b>p</b>erceptron) is a type of neural network composed of an input layer, one or more hidden layers, and an output layer. The hidden layers consist of neurons based on the McCulloch-Pitts mathematical model.

Each neuron (except those in the input layer) uses an activation function to introduce non-linearity. I chose the *tanh* function because it is symmetric around zero - unlike the sigmoid function, which tends to push outputs toward 0.5. With tanh, I noticed improved convergence during training.

The training process starts with forward propagation (also called feed-forward), where inputs move through the network using randomly initialized weights to compute outputs. The output is then compared to the expected result to compute the error. This is followed by backward propagation, where the error is used to update the weights in a way that reduces the overall loss.

I also included bias neurons in each layer to help shift activation values, allowing the network to better fit the training data.

# How to run?
```
git clone https://github.com/dziobex/simple-neural-network.git
cd simple-neural-network
mingw32-make
./neuro
```

# Preview
## 1 &oplus; 1
![](docs/1xor1.png)
```
./neuro     
Resourcer is being created.
Tests in total: 87
0.0 xor 1.0 = 1.0
0.0 xor 0.0 = 0.0
1.0 xor 0.0 = 1.0
1.0 xor 1.0 = 0.0
HANDLER is being destroyed
Resourcer is being destroyed.
```
## 0 &oplus; 1
![](docs/0xor1.png)
```
./neuro     
Resourcer is being created.
Tests in total: 115
1.0 xor 1.0 = 0.0
1.0 xor 0.0 = 1.0
0.0 xor 0.0 = 0.0
0.0 xor 1.0 = 1.0
HANDLER is being destroyed
Resourcer is being destroyed.
```

# Sources!
* https://home.agh.edu.pl/~horzyk/lectures/miw/MIW-SztuczneSieciNeuronoweMLP.pdf
* http://galaxy.agh.edu.pl/~vlsi/AI/bias/bias.html
* https://www.youtube.com/watch?v=-7scQpJT7uo
