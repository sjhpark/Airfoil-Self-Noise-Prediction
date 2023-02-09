# Airfoil-Self-Noise-Prediction

Predicting airfoil self-noise using machine learning and deep learning techniques

---
## Flow Conditions That Produce Airfoil Self-Noise
![image](https://user-images.githubusercontent.com/83327791/217485428-00f4bdd3-14ed-4977-a760-35d651cbb818.png)

## Dataset used: 
UCI Airfoil Self-Noise Data Set

https://archive.ics.uci.edu/ml/datasets/airfoil+self-noise#

The airfoil self-noise dataset has:
- 5 features (first 5 columns in the dataset):
    - Frequency [Hz]
    - Angle of attack [degrees]
    - Chord length [m]
    - Free-stream velocity [m/s]
    - Suction side displacement thickness [m]
- Output (last column in the dataset):
    - Sound Pressure Level [dB] 

## Feature Engineering & Pre-Processing
I have shuffled, Split, and Normalized the dataset.

## Multi-Layer Perceptron (MLP)
Created a feed-forward MLP to train. Used 4 hidden layers with ReLU activation function at each layer.
![image](https://user-images.githubusercontent.com/83327791/217498006-207a9f33-9876-4422-bd18-f2314ac05e93.png)

## Results
Achieved average MSE test error of 3.13 dB for the scaled sound pressure level after 500 epochs of training with batch size of 32 and learning rate of 0.0005. The average test error could get further reduced by removing the few outliers.

Used the weight decay of 1E-2 as L2 Regularization to prevent overfitting.

Mean Squared Loss was used as the loss function to calculate errors between the ground-truth and predicted sound pressure levels.

![image](https://user-images.githubusercontent.com/83327791/217778656-af354588-56a9-4963-81b0-09cf125645ba.png)

![image](https://user-images.githubusercontent.com/83327791/217778628-9bea0c23-dbd1-437a-88d2-f6aadfe23074.png)

![image](https://user-images.githubusercontent.com/83327791/217780972-f9876962-e38f-4410-b11f-b3c15e4b2973.png)

## References
[1] Thomas F. Brooks, D. Stuart Pope, and Michael A. Marcolini. Airfoil self-noise and prediction. NTRS Author
Affiliations: PRC Kentron, Inc., Hampton, NASA Langley Research Center NTRS Report/Patent Number: L-
16528 NTRS Document ID: 19890016302 NTRS Research Center: Legacy CDMS (CDMS). July 1989. url: https://ntrs.nasa.gov/citations/19890016302.

[2] Roberto Lopez. Airfoil Self-Noise Data Set. Mar. 2014. url: https://archive.ics.uci.edu/ml/datasets/airfoil+self-noise.

[3] Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

