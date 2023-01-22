# LINEAR SEARCH AND BINARY SEARCH : 

## AIM :

To write a program to perform linear search and binary search using python programming.

## EQUIPMENTS REQUIRED :
-	Hardware – PCs
-	Anaconda – Python 3.7 Installation / Moodle-Code Runner

## ALGORITHIM :

## LINEAR SEARCH :

1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.

## BINARY SEARCH :

1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high

## PROGRAM  :

# Use a linear search method to match the item in a list :
```python

Program for linear search method to match the item in a list
Developed by: MIDHUN AZHAHU RAJA P
RegisterNumber: 22008311

def linearSearch(array,n,k):
    for i in range(0, n):
        if array[i] == k:
            return i
    return -1
    
array = eval(input())
# sort the array
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
n = len(array)
array.sort()
result = linearSearch(array, n, k) # use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result == -1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ", result)
```
# Find the element in a list using Binary Search(Iterative Method).

```python
Program for linear search method to match the item in a list
Developed by: MIDHUN AZHAHU RAJA P
RegisterNumber: 22008311

def binarySearchIter(array, k, low, high):
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
    while low <= high:
        mid = low + (high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid] < k:
            low = mid + 1
        else:
            high = mid - 1
    return -1
    
array = eval(input())
# sort the array
array.sort()
k = eval(input()) #k-item to be searched
# use the binary search function to find the item in the list
result = binarySearchIter(array, k, 0, len(array)-1)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result == -1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ", result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).

```python
Program for linear search method to match the item in a list
Developed by: MIDHUN AZHAHU RAJA P
RegisterNumber: 22008311

def BinarySearch(arr, k, low, high):
    # Write your code here for binary search using recursive method
    if high >= low:
        mid = low + (high - low)//2
        if arr[mid] == k:
            return mid
        elif arr[mid] > k:
            return BinarySearch(arr, k, low, mid-1)
        else:
            return BinarySearch(arr, k, mid+1, high)
    else:
        return -1
    
    
arr = eval(input())
#sort the array
arr.sort()
k = eval(input()) # k is the element to be searched for
result = BinarySearch(arr, k, 0, len(arr)-1)# use the binary search function to find the result
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result == -1:
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ", result)

```

## INPUT :

### INPUT FOR LINEAR SEARCH :

![lin_sch_que](https://user-images.githubusercontent.com/118054670/213930750-96305512-c3e0-4612-b462-ee667ee6e63c.png)

### INPUT FOR BINARY SEARCH USING ITERATIVE METHODE :

![bin_sch_que1](https://user-images.githubusercontent.com/118054670/213930795-f6c020c5-1116-4881-9f3f-b382a5e17c46.png)

### INPUT FOR BINARY SEARCH USING RECURSIVE METHODE :

![bin_sch_que2](https://user-images.githubusercontent.com/118054670/213930831-9d47f182-1a5b-446c-8327-c4f23f194325.png)


## OUTPUT :

### OUTPUT LINEAR SEARCH :

![lin_sch](https://user-images.githubusercontent.com/118054670/213930891-72fe64f7-6b00-4dac-bf11-870759c31539.png)

### OUTPUT FOR BINARY SEARCH USING ITERATIVE METHODE :

![bin_sch_itr](https://user-images.githubusercontent.com/118054670/213930967-0b3a12a9-2a4f-410f-ad35-5bcdb71a1384.png)

### OUTPUT FOR BINARY SEARCH USING RECURSIVE METHOD :

![bin_sch_rec (1)](https://user-images.githubusercontent.com/118054670/213931010-97f7d0c3-fb48-4b55-b67b-08f8300f7645.png)

## RESULT :

Thus the linear search and binary search algorithm is implemented using python programming.
