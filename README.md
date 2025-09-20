## MNIST Demonstration

This project is designed to be a demonstration of a couple of different ideas.

1. Using a basic dataset, in this case the MNIST hand written digit dataset
2. Training and generalisation of a model to do classification
3. Training and generalisation of a model to do reconstruction

### Model

The model using a shared encoder which are a few residual CNN blocks. After encoding into a bottleneck, the model diverges along two paths. One path undoes the encoding to arrive back at a 28x28 image that is meant to be the reconstruction of a masked digit. The other path classifies on the bottleneck embedding.