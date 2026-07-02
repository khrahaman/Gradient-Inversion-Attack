**Gradient Inversion Attack:** 

An reverse-engineering framework where the actual training data-points can be reconstructed by only the output of a Neural Network.

**Security Concern:**

Suppose in a distributed learning framework (e.g., Federated Learning (FL)) a client trains a neural network locally and shares the training result only with the central server (such is the general workflow of FL). As the client is only sharing the training result, not the actual data-points (user data/ raw data) on which the neural network was trained, with the server; it might seem that there can be no exposure of the private data during the transmission (as the data-points are not leaving client-side). 
However, the introduction of gradient inversion attack proved that the training data-points can be reconstructed through the shared output only. For example, if a client trains a local neuarl network on image dataset and sahres the training result (e.g., gradient, updated model weights) only in the network, the attackers can achieve a truthful reconstruction of those training images with only the gradient.  
