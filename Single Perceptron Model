# -*- coding: utf-8 -*-
"""
Created on Mon Nov 20 13:26:57 2017

@author: Administrator
"""

import numpy as np


#Perceptron Initial parameters
weight = np.array([0,0])
bias = 0

#Training Data
x = np.array([[-1,1],[0,-1],[10,1]])  #inputs
y = np.array([1,-1,1])   #outputs


counter  = 0

while counter <2.5:           # Need to have correctly guessed all three outputs, for each correct guess the perceptron gets "1" added to the counter (see line 40).
    counter  = 0
    for i in range(3):
    
        guess = np.sum((weight*x[i])) + bias  # guess of the perceptron, need to pass through activation function
 
    
# Rectifier / Activation Function    
        if guess > 0:
            guess = 1
        elif guess < 0:
            guess = -1
        elif guess == 0:         # We consider a guess on the separating line a failure, kinda redundant.
            guess = 0
            
        if guess != y[i]:                 # If guess is wrong update the weights and bias according to this, moving the separating line
            weight = weight + y[i]*x[i]
            bias = bias + y[i]
        else:                              # If it's correct then add to the counter
            counter +=1
