# Ensai
Estimating parameters of strong gravitational lenses with convolutional neural networks.

This code uses convolutional neural networks (using tensorflow) to estimate the parameters of strong gravitational lenses. Unfortunetly we're not very good at coding, so you'll find that the code is messy, not well documented, and crazily written. However, that shouldn't discourage you from trying it out. Because it's a pretty pretty cool thing: The code can reover the parameters of gravitational lenses in a fraction of a second. Something that used to take hundreds of hours!


The results of this work have been published in a Nature letter "Fast Automated Analysis of Strong Gravitational Lenses with Convolutional Neural Networks" (Aug 31st, 2017).
In the next few months we'll be slowly making this code more user-friendly and extended it to more interesting and complex lensing configurations.

For those wanting to try it: The best place is to start by running the ipython notebook. It's a quick demonstration of lens modeling with neural networks. 
This is what you need:
1) A working version of python and tensorflow. This should be easy: a simple installation on your laptop could probabily just be done with pip. (https://www.tensorflow.org/install/)
2) The data: Unfortunately the file (specially the trained network weights) are too large to be hosted here. So we have put them here:
Please download these, untar them, and place them inside the "data/" folder. So at the end inside your "data" folder you should have a folder called "CosmicRays", another called "SAURON_TEST", and a third called "trained_weights" (in addition to the two files that are already there). 
3) With these you're good to go. You can run through the ipython notebook and model your first lenses with neural nets! Congratulation. 


 


If you'd like to get your hands a bit more dirty:
1) The data we proveded is just for fun. You can produce your own simulated data using this script: "src/Lensing_TrainingImage_Generator.m". This is a matlab script that contains all the required functions to generate simulated lenses. The only thing needed for this is a sample of unlensed images (e.g., from the GalaxyZoo, or GREAT3 datasets). 

2) You can use "init.py" to setup the models. Then with "single_model_predictions.py" you can get the predictions of a single network. Alternatively, after running "init.py". you can run "combo_prediction.py", to combine the 4 models (see the paper referenced above). If you'd like to train your own model, use "train.py". You can train the existing models (there're about 11 models defined in "ensai_model.py"), or just throw a bunch of layers together yourself and see if you come up with something magical. 



