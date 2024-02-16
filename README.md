# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: SHARAN M J
### Register Number: 212222240097


## Output:

### i) Read and display the image
```py
    import cv2
    image=cv2.imread('virat.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('virat',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-16 094827](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/817f7395-515c-4c2d-afed-3e42703e0a16)



### ii)Write the image
```py
    import cv2
    image=cv2.imread('virat.jpg',0)
    cv2.imwrite('king kholi.jpg',image)
```
## Output:

![Screenshot 2024-02-16 094839](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/053b3656-795f-4dd9-98fd-44fc47288d44)


### iii)Shape of the Image
```py
    import cv2
    image=cv2.imread('virat.jpg',1)
    print(image.shape)
```
## Output:
![Screenshot 2024-02-16 094854](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/5888a691-61ab-4770-b8f2-b68a29338057)


### iv)Access rows and columns
```py
    import random
    import cv2
    image=cv2.imread('virat.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('king kholi',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## Output:

![Screenshot 2024-02-16 102322](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/dce17986-5612-4ddb-a814-52631cd55bf3)


### v)Cut and paste portion of image
```py
   import cv2
   image=cv2.imread('virat.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('kingkholi1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
## Output:

![Screenshot 2024-02-16 102418](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/e64bbbad-4b75-44c4-88f2-416384a58198)

### vi) BGR and RGB to HSV and GRAY
```py
import cv2
img = cv2.imread('virat.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-16 102627](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/7f0e3ec6-ce74-4823-ae63-ce23fbc2b807)
![Screenshot 2024-02-16 102655](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/419dd741-3075-4fc3-8b6a-04ee32427727)
![Screenshot 2024-02-16 102701](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/16370280-39de-494f-9fba-424cb352ac39)
![Screenshot 2024-02-16 102706](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/6b11d3d2-3429-48c9-a9da-350128239c32)
![Screenshot 2024-02-16 102711](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/9639d543-2ef3-48df-ae07-dc960921a0d7)
### vii) HSV to RGB and BGR
```py
import cv2
img = cv2.imread('virat.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-16 102830](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/edf95a10-9514-43cb-8972-a7a4a41f3904)
![Screenshot 2024-02-16 102836](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/559ed0d9-fe15-41ca-9f01-b7e228cdf3aa)
![Screenshot 2024-02-16 102841](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/232f3369-8224-4915-8665-93eb258fe3d6)
### viii) RGB and BGR to YCrCb
```py
import cv2
img = cv2.imread('virat.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-16 102941](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/1d620961-1095-41fb-b3cf-dff99109e3e3)
![Screenshot 2024-02-16 102945](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/879cb7e1-f33e-4b79-b6ee-73e10be5d7c1)
![Screenshot 2024-02-16 102952](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/e8b3cda5-aa7c-4a05-8035-8ce913eb56a4)
### ix) Split and merge RGB Image
```py
import cv2
img = cv2.imread('virat.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-16 103123](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/fff9fca7-57bf-4c80-a7c0-73bfa10931f1)
![Screenshot 2024-02-16 103127](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/ada36b1f-9005-4367-805f-c7b0292f9896)
![Screenshot 2024-02-16 103133](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/2e6e9dfa-a299-4edc-9838-066c64c6aa76)
![Screenshot 2024-02-16 103137](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/b96f1378-459e-4306-89b3-e567ddbd44fa)

### x) Split and merge HSV Image
```py
import cv2
img = cv2.imread("virat.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-16 103249](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/c586487e-aa86-4b8b-bf4b-34bd108109c3)
![Screenshot 2024-02-16 103256](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/3115c0d7-9878-4109-9f08-996046590e8b)
![Screenshot 2024-02-16 103301](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/bcd26e5f-e352-4793-a08a-bb69bc85cbd1)
![Screenshot 2024-02-16 103306](https://github.com/SHARAN-MJ/COLOR_CONVERSIONS_OF-IMAGE/assets/119560305/b62cf06b-ec0d-4421-a181-77e02f453b1f)
## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
