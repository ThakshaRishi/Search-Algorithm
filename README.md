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
```
Program for linear search method to match the item in a list
Developed by:Thaksha Rishi
RegisterNumber: 23013212
def linearSearch(array,n,k):
    # write your code for linear search
    for i in range(n):
        if(array[i]==k):
            return i
    return -1
    
array = eval(input())
# sort the array
array.sort()
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
n=len(array)
result = linearSearch(array,n,k)# use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```


ii)	# Find the element in a list using Binary Search(Iterative Method).
``` 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Thaksha Rishi
RegisterNumber: 23013212
def binarySearchIter(array, k, low, high):
    while(low<=high):
        m=(low+high)//2
        if(array[m]==k):
            return m
        elif(array[m]<k):
            low=m+1
        else:
            high=m-1
    return -1
array = eval(input())
k = eval(input())
array.sort()
res=binarySearchIter(array,k,0,len(array)-1)
if(res==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",res)





```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Thaksha Rishi
RegisterNumber: 23013212
def BinarySearch(arr, k, low, high):
    if(low<=high):
        m=(low+high)//2
        if(arr[m]==k):
            return m
        elif(arr[m]<k):
            return BinarySearch(arr,k,m+1,high)
        else:
            return BinarySearch(arr,k,low,m-1)
    else:
        return -1
arr = eval(input())
k = eval(input())
arr.sort()
res=BinarySearch(arr,k,0,len(arr)-1)
if(res==-1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",res)





```
## Sample Input and Output
![Alt text](<Screenshot 2023-12-21 182010.png>)
![Alt text](<Screenshot 2023-12-21 182132.png>)
![Alt text](<Screenshot 2023-12-21 182146.png>)
![Alt text](<Screenshot 2023-12-21 182229.png>)
![Alt text](<Screenshot 2023-12-21 182246.png>)
![Alt text](<Screenshot 2023-12-21 182311.png>)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.