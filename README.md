# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages.

### Step2:
Create the Text using cv2.putText.
### Step3:

Create the structuring element.
### Step4:

Erode and Dilate the image.
### Step5:

End Program.
 
## Program:

``` Python
# Import the necessary packages

import cv2
import matplotlib.pyplot as plt
import numpy as np

# Create the Text using cv2.putText

img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
cv2.putText(img1,'Navya',(5,70),font,2,(255),5,cv2.LINE_AA)


# Create the structuring element

kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image

image_erode=cv2.erode(img1,kernel)
plt.imshow(image_erode)
plt.axis('off')
plt.title('Erosion')


# Dilate the image

image_dilate=cv2.dilate(img1,kernel)
plt.imshow(image_dilate)
plt.axis('off')
plt.title('Dilation')




```
## Output:

### Display the input Image

![GITHUB](d2.PNG)

### Display the Eroded Image

![GITHUB](d.PNG)

### Display the Dilated Image

![GITHUB](d1.PNG)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.