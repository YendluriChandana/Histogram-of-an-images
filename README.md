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
```python
# Developed By: Yendluri Chandana
# Register Number: 212223100063
import cv2
import matplotlib.pyplot as plt

# Histogram for Gray scale and Color image
 
gray_image = cv2.imread('grayscale.jpeg')
color_image = cv2.imread('color.jpeg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()



# Equalized Image
import cv2
Gray_image=cv2.imread('gray.jpeg',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/YendluriChandana/Histogram-of-an-images/assets/139842204/b76b891e-66b5-4ad2-9c76-a185ec597c34)


### COLOR IMAGE:
![image](https://github.com/YendluriChandana/Histogram-of-an-images/assets/139842204/a388e6a5-58cb-45eb-8b72-c6139a498623)





### Histogram of Grayscale Image and any channel of Color Image
### GREY SCALE :
![image](https://github.com/YendluriChandana/Histogram-of-an-images/assets/139842204/ca4081a3-6155-43bb-b999-a9b69f687c86)

## COLOR SCALE IMAGE:
![image](https://github.com/YendluriChandana/Histogram-of-an-images/assets/139842204/5a5bd114-439b-42f2-97ce-c58fd03c3818)


### Histogram Equalization of Grayscale Image.

### ORIGINAL:
![image](https://github.com/YendluriChandana/Histogram-of-an-images/assets/139842204/8c5a716c-0410-4ff2-b69d-4f42bd948ca0)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
