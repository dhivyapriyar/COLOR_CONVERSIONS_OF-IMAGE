# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By: Dhivyapriya. R
### Register Number: 212222230032
### i)Read and Display an Image
Load an image from your local directory and display it
```
import cv2 
image=cv2.imread('image.jpg',1)
image =cv2.resize(image, (506, 317))
cv2.imshow('WINDOW',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/793d9ace-84fa-4773-b51a-93631d997617)

### ii)Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("image.jpg")
image = cv2.resize(image, (506, 317))
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/bb6a3c1c-0085-4bdb-907b-c3a45b41e68b)

(2) Draw a circle at the center of the image.
```
import cv2
image = cv2.imread("image.jpg")
image = cv2.resize(image, (506, 317))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/c49cba5c-524f-4936-9b4e-a4e67628096b)

(3) Draw a rectangle around a specific region of interest in the image.
```
import cv2
image = cv2.imread("image.jpg")
image = cv2.resize(image, (506, 317))
start = (150, 100)
stop = (300, 200)
color = (255, 255, 100)
thickness = 10           
res_img = cv2.rectangle(image, start, stop, color, thickness)
cv2.imshow('WINDOW', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/af1372af-c145-4235-bca0-92c8824e7822)

(4) Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("forest.png")
image = cv2.resize(image, (400, 300))
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![image](https://github.com/user-attachments/assets/a1735a18-b215-4550-843a-ca52519035ee)


### iii)Image Color Conversion

(1) Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/d82611e2-a7b4-4d46-9b8c-387c938d1791)

![image](https://github.com/user-attachments/assets/dda080ae-7665-4dab-9715-833e6cc3484b)

(2) Convert the image from RGB to GRAY and display it.
```
import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![image](https://github.com/user-attachments/assets/54af937e-eabf-4ecf-b464-6be0c74475f0)

![image](https://github.com/user-attachments/assets/3177d734-9103-462d-ac52-0d458d9c1400)

(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/568029da-32de-488f-84be-02dd13b71ec6)

![image](https://github.com/user-attachments/assets/3523f164-5bc3-40b5-adb3-3a847d0fb418)

(4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/ac4c362b-dba0-4169-9373-bb0fbc043e50)

![image](https://github.com/user-attachments/assets/ff8e8bbd-bc1f-49bd-befa-6a8833261508)

### iv)Access and Manipulate Image Pixels

(1) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/b4ec5ca1-daff-404f-8054-9990c74051ec)

(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/26ea1c05-3218-4dab-b8f4-980b3bb69da3)

![image](https://github.com/user-attachments/assets/66a0442f-0426-4c77-967c-aef72bcd7125)

### v)Image Resizing
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/190093a2-86e8-4dae-9db3-1ac785eb83d5)

![image](https://github.com/user-attachments/assets/e77172f8-5d16-4389-b8a0-e5627a4f9e67)


### vi)Image Cropping

Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/884ed906-804b-418c-a156-a885adae7141)

### vii)Image Flipping
(1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("forest.png")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/e7b63749-75d0-45c9-aa97-4e522afe0abf)

![image](https://github.com/user-attachments/assets/0d427c7b-eab4-41fe-ba69-fb0684788f34)

(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("forest.png")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![image](https://github.com/user-attachments/assets/a55de34a-e30d-48a7-9787-cd46a7f8be7b)

![image](https://github.com/user-attachments/assets/8061bca9-5c2d-4f86-a384-69b2ad41196a)

### viii)Write and Save the Modified Image

Save the final modified image to your local directory.

```
import cv2
img = cv2.imread("forest.png")
img = cv2.resize(img,(300,200))
cv2.imwrite('boat_pic.jpg',img)
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/4c808c4b-ee3e-4f38-b5fa-f061135bff3c)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







