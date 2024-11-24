# EX 10 OPENING AND CLOSING
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
NAME: Vasanth P
Reg No:212222240113
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
cv2.putText(img1,'Vasanth',(5,70), font,2,(255),5,cv2.LINE_AA)
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
```python'
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```


## Output:
### Display the input Image
![image](https://github.com/user-attachments/assets/fb6f9b12-64d1-4a8c-b301-1cf988201b2e)



### Display the result of Opening
![image](https://github.com/user-attachments/assets/dff5457f-f14c-40ed-88a0-aa3145423f74)

### Display the result of Closing
![image](https://github.com/user-attachments/assets/a5094774-ae16-466e-b322-b64c4b24befa)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
