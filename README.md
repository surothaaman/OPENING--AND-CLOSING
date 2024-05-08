# EX.NO:10 OPENING--AND-CLOSING
# DATE:
## Aim
To implement Opening and Closing using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Give the input text using cv2.putText()
- Step3: Perform opening operation and display the result
- Step4: Similarly, perform closing operation and display the result
## Program:
```
DEVELOPED BY:SUROTHAAMAN R
REGISTER NUMBER:212222103003
``` 
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'IMAGE',(5,70), font,2,(255),5,cv2.LINE_AA)
```
# Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
```python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
# Use Closing Operation
```python
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:
### Display the input Image
![image](https://github.com/gpavana/OPENING--AND-CLOSING/assets/118787343/f2fa1602-61c9-42e5-9835-8dc176454214)
### Display the result of Opening
![image](https://github.com/gpavana/OPENING--AND-CLOSING/assets/118787343/aaa3ac56-e403-40a4-9272-8dc8e71e942c)
### Display the result of Closing
![image](https://github.com/gpavana/OPENING--AND-CLOSING/assets/118787343/fb640a34-1968-43aa-8581-01adc438d5ec)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
