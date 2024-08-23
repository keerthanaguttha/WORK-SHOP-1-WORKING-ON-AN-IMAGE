# WORK-SHOP-1-WORKING-ON-AN-IMAGE
WORKSHOP-1 WORKING ON  AN IMAGE
## AIM:
TO WORK ON AN IMAGE.
## STEPS :
```
1.Load two images of the same size.
2.Divide each image into four equal regions (quadrants) based on specific row and column coordinates.
3.Save the eight individual regions, labeling them as R1, R2, R3, R4 for the first image and R5, R6, R7, R8 for the second image.
4.Swap the regions as follows:
5.R1 with R8
6.R2 with R7
7.Resize the final images to dimensions specified by the last four digits of your registration number, ensuring the number is even.

```

## PROGRAM:
### STEP 1:
import cv2
### STEP 2:
READ THE IMAGES:
```
image1 = cv2.imread("dip1.jpg")
image2 = cv2.imread("dip2.jpg")
```
### STEP 3:
ENSURE SIZE OF THE RESPECTIVE IMAGES ARE SAME:
```
image1.shape
image2.shape
```
### STEP 4:
FIND THE HEIGHT,WIDTH,MID POINT OF ROW AND COLUMN . ASSSUME VARIABLES AND ASSIGN THEM AS R1,R2,R3,R4 FOR IMAGE1 AND R5,R6,R7,R8 FOR IMAGE2
```
R1 = image1[0:300, 0:400]     
R2 = image1[0:300, 400:800] 
R3 = image1[300:600, 0:400] 
R4 = image1[300:600, 400:800] 

R5 = image2[0:300, 0:400]     
R6 = image2[0:300, 400:800] 
R7 = image2[300:600, 0:400] 
R8 = image2[300:600, 400:800]
```
### STEP 5:
WRITE THE IMAGES WHICH ARE SPLITTED
```
cv2.imwrite('r1.jpg',R1)
cv2.imwrite('r2.jpg',R2)
cv2.imwrite('r3.jpg',R3)
cv2.imwrite('r4.jpg',R4)

cv2.imwrite('r5.jpg',R5)
cv2.imwrite('r6.jpg',R6)
cv2.imwrite('r7.jpg',R7)
cv2.imwrite('r8.jpg',R8)
```
### STEP 6:
SWAP R1 WITH R8,R7 WITH R3
```
image1[0:300, 0:400]  =R8
image2[300:600, 0:400]  =R3

cv2.imshow('Swapped image1',image1)
cv2.imshow('Swapped image2',image2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
SHAPE:

![image](https://github.com/user-attachments/assets/e334d3ca-0a52-4499-9bd7-6dfb4495fc9a)

WRITE:

![image](https://github.com/user-attachments/assets/eacb78a0-2388-4fab-87e3-199792eef26b)


SWAPPED IMAGES:

![Screenshot 2024-08-23 215621](https://github.com/user-attachments/assets/5db62135-dbd0-4fc8-8f48-ad9f4e3753c9)

## RESULT:
Hence Swapped quadrants between two images is successful.
