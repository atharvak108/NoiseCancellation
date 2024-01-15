# NoiseCancellation
This repository contains all the codebase for my deep learning based noise cancellation project.

Pipelinefordrive contains the code used for processing audio files and converting it into log spectrograms and storing it in the drive.

ANC_CNN_LST contains the code used for training a CNN-LSTM-FCC Hybrid Deep Learning model to predict masks.

The first step was data collection, the data was collected in two separate measures, 
1. Background noise data
2. Background noise data combined with a person speaking

The area for data collection was the atrium lobby where all the noise would be collected in my college campus.

In logic the goal was to implement the cocktail party problem but instead of two noises here, we had 'n' distinct background noises. So for this, soft masking was used which is basically a ratio mask calculated through the combined noise and also the original background noise. 

Then these masks are multiplied with the combined noise and you get the clear noise.
Thus can a deep learning model predict a optimal mask ?

Yes, we did test the following through our hybrid CNN-LSTM-FCC architecture neural network which extracted the features and also the temporal dependencies amongst them and were able to predict the mask successfully. 
