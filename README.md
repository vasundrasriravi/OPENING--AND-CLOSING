# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

<br>Import the necessary packages


### Step2:
<br>Give the input text using cv2.putText()

### Step3:
<br>Perform opening operation and display the result

### Step4:
<br>Similarly, perform closing operation and display the result

 
## Program:
```
NAME: VASUNDRA SRI R
REG.NO: 212222230168
``` 
# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'ARTIFICIAL',(5,70), font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1)
plt.axis('off')
```
# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
```
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
# Use Closing Operation
```
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")

```
## Output:

### Display the input Image

![Screenshot 2024-04-19 122103](https://github.com/vasundrasriravi/OPENING--AND-CLOSING/assets/119393983/1e4e1ccb-2851-4e43-b5cd-83f9b43466e7)

### Display the result of Opening

![Screenshot 2024-04-19 122115](https://github.com/vasundrasriravi/OPENING--AND-CLOSING/assets/119393983/d9c74966-0029-4d10-b2f0-8f9ec5fc2506)


### Display the result of Closing

![Screenshot 2024-04-19 122136](https://github.com/vasundrasriravi/OPENING--AND-CLOSING/assets/119393983/eae03717-f3fe-4f6b-bff1-386cba816c5c)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
