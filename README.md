# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
### Developed By: KOWSALYA M
### Register Number: 212222230069
### Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt
gray_image=cv2.imread('rabbit.jpeg')
grey=cv2.cvtColor(gray_image,cv2.COLOR_BGR2GRAY)
plt.imshow(grey)
plt.axis('on')
plt.show()


color_image=cv2.imread('fish.jpeg')
plt.imshow(color_image)
plt.axis('on')
plt.show()
```
### Histogram of Grayscale Image and any channel of Color Image
```
import numpy as np
Gray_image = cv2.imread("rabbit.jpeg")
Color_image = cv2.imread("fish.jpeg")
grey=cv2.cvtColor(gray_image,cv2.COLOR_BGR2GRAY)
gray_hist = cv2.calcHist([grey],[0],None,[1100],[0,1100])
plt.figure()
plt.imshow(grey)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()


color_hist = cv2.calcHist([Color_image],[0],None,[2600],[0,2600])
plt.figure() 
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
```
### Histogram Equalization of Grayscale Image.
```
gray_image = cv2.imread("rabbit.jpeg")
grey=cv2.cvtColor(gray_image,cv2.COLOR_BGR2GRAY)
plt.imshow(grey)
plt.show()


equ = cv2.equalizeHist(grey)
plt.imshow(equ)
plt.show()


color_image=cv2.imread('fish.jpeg')
grey=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
plt.imshow(color_image)
plt.show()


eq = cv2.equalizeHist(grey)
plt.imshow(eq)
plt.show()
```

## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/321f7b52-9cb5-4018-bcfe-b6721c9b61d0)

![image](https://github.com/user-attachments/assets/7de8f133-88a3-447c-b564-47ea333516ee)


### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/user-attachments/assets/dac17c5f-1335-4006-8515-4ccaeaa96012)

![image](https://github.com/user-attachments/assets/ff00dcab-e0ab-4aa3-beab-d2ea1fc7d3b5)

![image](https://github.com/user-attachments/assets/38731a81-d10a-4f1d-8ba3-fe1beff40ef8)

![image](https://github.com/user-attachments/assets/c65c4bab-f84a-4106-8820-57c13bbc7ba1)


### Histogram Equalization of Grayscale Image.

![image](https://github.com/user-attachments/assets/c81e4085-8619-4942-93c2-5036f79f209e)

![image](https://github.com/user-attachments/assets/5de41752-f37e-4657-956a-086b5badc899)

![image](https://github.com/user-attachments/assets/6e2fd9fd-3243-4528-b9d4-9c489b6e309b)

![image](https://github.com/user-attachments/assets/8de20c2e-9f02-42a1-9471-c3e4a07c1403)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
