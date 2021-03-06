CPHRANN Workshop, Session 2
================

The TensorFlow Playground
-------------------------

TensorFlow playground allows us to tinker with a neural network to get a better understanding of what is going on.

### Part I

1.  Go to [TensorFlow Playground](https://playground.tensorflow.org)
2.  Choose only features `X_1` and `X_2`
3.  Remove all hidden layers by clicking `-` next to 'HIDDEN LAYERS'
4.  Change activation from `Tanh` to `Sigmoid`, this means that we are now fitting `s(w_1x_1 + w_2_x_2 + b)`, i.e. a logistic regression
5.  Click the 'play' symbol in the upper left corner, which will start the training
6.  Are we able to model the data?

<details><summary>Click here, when you are done thinking</summary> No, if you look at the data on the right, it's evident that a sigmoid function on untransformed input variables will not be able to create the needed discrimination </details>

### Part II

1.  Choose only features `X_1^2` and `X_2^2`
2.  Check that we are still using `Sigmoid` activation
3.  Click the 'play' symbol in the upper left corner, which will start the training
4.  Are we able to model the data? What happened?

<details><summary>Click here, when you are done thinking</summary> What happened here, was that we used our experience to look at the data and then transform the input variables. This is known as feature engineering. </details>

### Part III

1.  Choose only features `X_1` and `X_2`
2.  Add 2 hidden layers with 4 neurons each by clicking `+` next to 'HIDDEN LAYERS' and `+` above each set of neurons
3.  Are we able to model the data? What happened?

<details><summary>Click here, when you are done thinking</summary> What happened here, was that by adding complexicity to our model, we are now able to approximate the transformed variables we were working with in part II. The idea here being that in complex systems, often it is not clear if and how you need to transform your variables and the ANN will take care of that. </details>

### Part IV

1.  With the current setup, change the activation function to `ReLU`
2.  What happened with the decision boundaries?
3.  Change the number of neurons in the first layer to 3 and the number of neurons in the second layer to 2
4.  What happened with the decision boundaries?

<details><summary>Click here, when you are done thinking</summary> Sigmoid activation has the problem, that with small and large values, the gradient is close to zero, meaning that weights change very little. When using `ReLU` activation, this is no longer an issue and the model converges much more efficient with fewer epochs. From the decision bounadaries, you can see, that using the `ReLU` function corresponds to creating decision boundaries by joining linear segments and adding more neurons corresponds to adding more linear segments to perform the discrimination. </details>

### Part V

1.  Take 5 minutes to play around with TensorFlow Playground
