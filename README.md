# Multi-Class-Prediction-with-Kolmogorov-Arnold-Networks-KAN
Multi-Class Prediction with Kolmogorov-Arnold Networks (KAN)

This notebook applies the Kolmogorov-Arnold Networks (KAN) architecture to visual stimulus prediction in mice, given the firing rates of single neurons.
The model predicts what image the mouse is being shown out of 118 images. The data consists of spike-trains containing the total spikes each neuron fired when each image was shown, with around 2000 neurons each. 

This model's highest accuracy was ~75%, where an accuracy of ~0.85% would be a total guess. The model was found to work best with only one KAN layer connecting the input and output dimensions. This means only one activation function was found to transform the dataset. Although running PCA before this layer, with principal components roughly the same number of components as the number of classes, allowed the model to perform faster and with a diminished accuracy. This performed worse than models, like LSTMs or ST-GATs, that can account for temporal and spatial dependencies. However, the ability to show inference between the effect of individual neurons and the possibility to network effects might create a niche for Kolmogorov-Arnold Networks to be used in future studies.
