# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image.

### Step5:
Reflect of image.

### Step6:
Rotate the image


## Program:
```
Developed By: KATHIRVEL.A
Register Number:212221230047

i)Original Image:
# To show the original image and to find the shape of the image
import cv2
import numpy as np
img = cv2.imread('prof.jpg',-1)
original = cv2.cvtColor(img , cv2.COLOR_BGR2RGB)
cv2.imshow('input',original)
cv2.waitKey(0)
cv2.destroyAllWindows()
original.shape
row, col, dim =original.shape

ii)Image Translation

translation = np.float32([[1,0,100],[0,1,150],[0,0,1]])
translated_image = cv2.warpPerspective(original,translation,(col,row))
cv2.imshow('translated_image',translated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

iii)Image shearing

shear_x = np.float32([[1,0.7,0],[0,1,0],[0,0,1]])
shear_y = np.float32([[1,0,0],[0.3,1,0],[0,0,1]])
sheared_x= cv2.warpPerspective(original,shear_x,(col,row))
sheared_y = cv2.warpPerspective(original,shear_y,(col,row))
cv2.imshow('shear_x',sheared_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('shear_y',sheared_y)
cv2.waitKey(0)
cv2.destroyAllWindows()



iv)Image Reflection

ref_x = np.float32([[1,0,0],[0,-1,row],[0,0,1]])
ref_y = np.float32([[-1,0,col],[0,1,0],[0,0,1]])
reflect_x= cv2.warpPerspective(original,ref_x,(col,row))
reflect_y = cv2.warpPerspective(original,ref_y,(col,row))
cv2.imshow('reflected_x',reflect_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('reflected_y',reflect_y)
cv2.waitKey(0)
cv2.destroyAllWindows()



v)Image Rotation

angle = np.radians(15)
mat_rotate = np.float32([[np.cos(angle),-
(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotate_img =cv2.warpPerspective(original,mat_rotate,(col,row))
cv2.imshow('rotated',rotate_img)
cv2.waitKey(0)
cv2.destroyAllWindows()





vi)Image Cropping

cropped_img=img[10:500,25:600] 
cv2.imshow('after_cropping',cropped_img);
cv2.waitKey(0)
cv2.destroyAllWindows()


```




## Output:






###Original Image:



![image](https://github.com/KathirvelAIDS/IMAGETRANSFORMATION/assets/94911373/6e0a8d21-702a-478d-a527-3553e7423753)




### i)Image Translation


![image](https://github.com/KathirvelAIDS/IMAGETRANSFORMATION/assets/94911373/d7363cf9-6139-4da4-a9b7-5c9193055cbf)






### ii) Image Scaling


![image](https://github.com/KathirvelAIDS/IMAGETRANSFORMATION/assets/94911373/e472f831-4560-4aa3-a25a-e9cbdb7ad6b9)




### iii)Image shearing


![image](https://github.com/KathirvelAIDS/IMAGETRANSFORMATION/assets/94911373/f4ad548a-0274-4935-90e9-b3c72edb096c)





### iv)Image Reflection



![image](https://github.com/KathirvelAIDS/IMAGETRANSFORMATION/assets/94911373/20eea4fe-b954-4581-bd98-5d704412fb01)



### v)Image Rotation


![image](https://github.com/KathirvelAIDS/IMAGETRANSFORMATION/assets/94911373/3a890086-fa11-4f9d-8c44-f9f30faa73ac)




### vi)Image Cropping


![image](https://github.com/KathirvelAIDS/IMAGETRANSFORMATION/assets/94911373/c23c9aa5-a1f9-4af1-ab0c-da885375b6b9)


![image](https://github.com/KathirvelAIDS/IMAGETRANSFORMATION/assets/94911373/c60ab74e-7ff0-41ce-a380-3e025d6aab94)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
