# sudokuSolver
in this prj we are able to solve the sudoku without our brain and with just using openvc and our PC to process and solve the table 

# libraries
tensorflow , os , opencv , keras 

import cv2

import numpy as np

from tensorflow.python.keras.models import load_model

notice! = if you are using macbook m1 you also need ( tensorflow-macos, tensorflow-metal )

# Test Image
 sample 1
 
![](https://github.com/mohammadst99/sudokuSolver/blob/main/test/test1.png)


 sample 2
 
![](https://github.com/mohammadst99/sudokuSolver/blob/main/test/test2.png)


# Code explain 

first we need to add our photo with cv2 

then we need to apply filter ( gray , blur , canny) so that we can find the contours 

next step we need to find the biggest contour to find exactly our full table including other small tables 

as we find the table we change the perspective to pick the table from our full image in order to process

then we have to divide this picked image to 9 column and 9 row ( in total 81 box ) that each box might including a number or might be empty

then we use tensorflow.keras.models and our model to predict the number in each box

then we put the numbers in a list and we put 0 for each box which was empty 

then we use the other python file library(sudoku_solverMath) to solve the sudoku , we have to send our sudoku as a list to it and then this  library provide us an list again which was solved our table and finally we apply the solvation to our image 

