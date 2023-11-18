# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```''' 
Program for linear search method to match the item in a list
Developed by: LINGESWARAN K
RegisterNumber: 212222110022
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
array = eval(input())
# sort the array
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
n=len(array)
array.sort()
result = linearSearch(array,n,k)
# use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: LINGESWARAN K
RegisterNumber: 212222110022
'''
def binarySearchIter(array, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return binarySearchIter(arr,k,low,mid-1)
        else:
            return binarySearchIter(arr,k,mid+1,high)
    else:
        return -1
arr = eval(input())
# sort the array
arr.sort()
k = eval(input()) #k-item to be searched
result = binarySearchIter(arr,k,0,len(arr)-1)
if result==-1:
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: LINGESWARAN K
RegisterNumber: 212222110022
'''
def BinarySearch(arr, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
arr = eval(input())
#sort the array
arr.sort()
k = eval(input())# k is the element to be searched for
# use the binary search function to find the result
result = BinarySearch(arr,k,0,len(arr)-1)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result==-1:
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)
```
## Sample Input and Output
i) #Use a linear search method to match the item in a list.
![image](https://github.com/Lingeswaran04/Search-Algorithm/assets/119103865/4d0e12ab-9516-43c5-be82-614fc3890ec2)
ii)	# Find the element in a list using Binary Search(Iterative Method).
![image](https://github.com/Lingeswaran04/Search-Algorithm/assets/119103865/d5583c7d-66d3-41d8-8aaa-087a6d5e6d44)
iii)	# Find the element in a list using Binary Search (recursive Method).
![image](https://github.com/Lingeswaran04/Search-Algorithm/assets/119103865/98abd586-d310-4a98-bbc2-3eb7f272ddd6)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
