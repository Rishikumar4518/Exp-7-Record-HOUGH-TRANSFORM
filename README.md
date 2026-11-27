## HOUGH-TRANSFORM
## Developed By
## Name : RISHI KUMAR E V
## Reg No : 212225240067
## Aim
To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

## Learning Objective
Understand each stage of image processing

Learn how to build a complete computer vision pipeline

Practice writing code in guided sections

## Software Used
Anaconda – Python 3.7

Jupyter Notebook / VS Code

OpenCV (cv2)

NumPy

Matplotlib

## Algorithm & Explanation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt


image = cv2.imread('1.jpg')



gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)



plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Input Image")
plt.axis('off')



plt.imshow(gray_image, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')

edges = cv2.Canny(gray_image, 50, 150)


plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')


lines = cv2.HoughLinesP(edges, 1, np.pi / 180, 100, minLineLength=50, maxLineGap=10)


for line in lines:
    x1, y1, x2, y2 = line.reshape(-1) 
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2) 


plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Result of Hough Transform")
plt.axis('off')

```
## output
## Original Image
<img width="347" height="462" alt="image" src="https://github.com/user-attachments/assets/11df8bb8-59e9-4ca8-97ca-3c88785635a4" />

## Grayscale Image
<img width="343" height="460" alt="image" src="https://github.com/user-attachments/assets/36608d32-7c45-4449-8212-906874702054" />


## Canny Edge Detector
<img width="342" height="466" alt="image" src="https://github.com/user-attachments/assets/9bd0413b-c763-4b0b-8ece-7d631a184142" />


## Result Of Hough Transform
<img width="341" height="467" alt="image" src="https://github.com/user-attachments/assets/31d15ceb-73d6-4325-9218-5c8dc6b9c495" />




## Result
Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively
