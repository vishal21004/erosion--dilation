## EX -09: Implementation-of-Erosion-and-Dilation
### NAME : VISHAL M.A
### REG NO : 212222230177
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the Image

### Step5:
Dilate the Image

 
## Program:


# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'ELBAF',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```


# Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```


# Erode the image
```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```



# Dilate the image
```python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![image 2](https://github.com/vishal21004/erosion--dilation/assets/119560110/6fd9d038-8092-4af2-be07-6acb3283586d)



### Display the Eroded Image
![image 4](https://github.com/vishal21004/erosion--dilation/assets/119560110/e9e36907-1429-47e8-b3f3-a252a8842ddd)



### Display the Dilated Image
![image 1](https://github.com/vishal21004/erosion--dilation/assets/119560110/7d342f70-3c4f-4ba9-ad0b-451e7861a8a3)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
