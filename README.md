# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Load the input image using cv2.imread().

### Step2:
Define a structuring element (e.g., 5x5 rectangular) using cv2.getStructuringElement().

### Step3:
Perform erosion followed by dilation using cv2.morphologyEx() with the cv2.MORPH_OPEN operation.

### Step4:
Perform dilation followed by erosion using cv2.morphologyEx() with the cv2.MORPH_CLOSE operation.

### Step5:
Use plt.subplot() to show the original, opening, and closing images side by side.

 
## Program:

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt
#i) Create the Text using cv2.putText
img1=np.zeros((300,700),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Mahajanani.R ",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()
#ii) Create the structuring element
#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))
#iii) Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()
#iv) Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:

### Display the input Image
![exp10op1](https://github.com/user-attachments/assets/d0718aca-45aa-45e5-b309-deb23cc9dd95)


### Display the result of Opening
![exp10op2](https://github.com/user-attachments/assets/5adae3f2-7ba3-45a6-be46-4402e6eac42a)


### Display the result of Closing
![exp10op3](https://github.com/user-attachments/assets/63359934-79f3-4e58-89b4-2595204ccdac)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
