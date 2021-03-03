# Name: Sriya Chettebhaktula
# Roll Number: 2019BCS-063
# Problem Statement :
# Write the code to calculate the spatial position with respect to frame {A} when the postion in frame {B} is represnted by 
# [2,3,0] and b is rotationg aroung x axis by 30 degree , x axis by 30 degree , y axis by 30 degree. 
# Write the final postion with respect to frame A.

import numpy as np

#Enter 3 coordinates with spaces in between
coord = np.array(list(map(float, input("Enter Initial co-ordinates: ").split()))).reshape((3, 1))

#Enter the angles in degrees
angX = np.deg2rad(float(input("Enter rotation about X : ")))
angY = np.deg2rad(float(input("Enter rotation about Y : ")))
angZ = np.deg2rad(float(input("Enter rotation about Z : ")))

rotnX = np.array([[1, 0, 0],[0, np.cos(angX), -np.sin(angX)],[0, np.sin(angX), np.cos(angX)]])
rotnY = np.array([[np.cos(angY), 0, np.sin(angY)],[0, 1, 0],[-np.sin(angY), 0, np.cos(angY)]])
rotnZ = np.array([[np.cos(angZ), -np.sin(angZ), 0],[np.sin(angZ), np.cos(angZ), 0],[0, 0, 1]])

rotn = ((rotnX @ rotnY) @ rotnZ)
print("New coordinates: ", rotn@coord)
