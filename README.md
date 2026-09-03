# Pelicia-Mikhail-Anthony-Bennet-D.R.---PA_2
### Name: PELICIA, Mikhail Anthony Bennet D.R.
### Section: 2ECE-C
### Date Submitted: 03/09/2026

## Problem A. Reproducible Normalization Problem
#### The instructions for this problem is to normalize a random 5x5 array. Using "np.random.seed(2112)" to make sure the random numbers are rerpoducible, "X = np.random.randint(10, 101, size=(5,5))" to make the 5x5 array with integers from 10-100, then using X.mean to get the mean and X.std to get the standard deviation which are both used to calculate the the normalized values in "X_normalized = (X - X.mean()) / X.std()", and "np.save" to save the array.
#### Here's the code that was used:
````
#This makes sure that the random numbers are reproducible
np.random.seed(2112)
X = np.random.randint(10, 101, size=(5,5))
X

#This normalizes the array
X_normalized = (X - X.mean()) / X.std()
#This prints the normalized array
print(X_normalized)

#This saves the normalized array as "X_normalized.npy"
np.save('X_normalized.npy', X_normalized)
````
## Problem B. Cubes Divisible by 4 Problem
#### The objective for this problem is to create a 10x10 array with integers from 1 - 100, cube all the values, and obtain all the values divisible by 4. To do this,  using "np.arrange(1,101) to create an array with the integers of 1-100, then ".reshape" to turn it into a 10x10 matrix, and "%4 == 0" to determine if it's divisible by 4, and np.save to save the array.
#### Here's the code that was used:
````
#This creates an array 
hundred = np.arange(1,101)
#This squares the numbers and shapes the array into a 10X10 grid
tenXten = hundred.reshape(10, 10) **2
tenXten

#This determines all the elements that are divisible by 4
div_by_4 = tenXten[tenXten % 4 == 0]

#This saves the array as "div_by_4.npy"
np.save('div_by_4.npy', div_by_4)
div_by_4
````
##Problem C. Above-Mean Square Problem
#### For this problem, the requirement was to create an array with the integers from 1-36, square the values, get the mean, and obtain the values that are greater than the mean. For this, "np.aranage" was used to create the matrix with "**2" to square the values, ".reshape" to make a 6x6 matrix, "np.mean" to get the mean of the matrix, "S[S > S_mean]" to get the values above the mean, and ".shape" to get the shape of the above_mean.
#### Here's the code that was used:
````
#This creates an array from 1-36, squares the elements, and arranges them in a 6x6 matrix
S = np.arange(1, 37) ** 2   
S = S.reshape(6, 6)

S

#This calculates the mean
S_mean = np.mean(S)
S_mean

#This sets the value above the mean for checking
above_mean = S[S > S_mean]
print(above_mean)
#This gets the shape of above_mean
above_mean.shape
````
