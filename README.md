# Solving-Mathematical-equation-Handwritten using CNN
 Handwritten Equation Solver trained by handwritten digits and mathematical symbol using Convolutional Neural Network with some image processing techniques
 
Equation can contain any digit from 0-9 and symbol +,x,- Works on image with white background and digits/symbols are in black.

You can run all the three ipynb files either separately or sequentially.

1. For running Data_extraction.ipynb first download train images.rar zip file and extract it in the folder containing Data_extaction.ipynb file.
2. For running model_training.ipynb, you either need to download train_final.csv or you can run it after succesfully running Data_extraction.ipynb.
3. For running CNN_test.ipynb, you either need to download model_final.h5 and model_final.json file or you can run it after succesfully running model_training.ipynb file. You also need to replace the path of the image in code from the local path of image to be tested on your computer.

![sub](https://github.com/innovator-arjun/Solving-Mathematical-equation-Handwritten-CNN/blob/main/sub.jpg)

1. Input an image containing a handwritten equation. Convert the image to a binary image and then invert the image(if digits/symbols are in black).
2. We obtain contours of the image by default, it will obtain contours from left to right.
3. Obtain bounding rectangle for each contour.
4. Sometimes, we may get two or more contours for the same digit/symbol. To avoid that, we can check if the bounding rectangle of those two contours overlaps or not. If they overlap, then discard the smaller rectangle.
5. Now, resize all the remaining bounding rectangle to 28 by 28.
6. Using our model, predict the corresponding digit/symbol for each bounding rectangle and store it in a string.
7.After that use ‘eval’ function on the string to solve the equation.

![output](https://github.com/innovator-arjun/Solving-Mathematical-equation-Handwritten-CNN/blob/main/output.PNG)
