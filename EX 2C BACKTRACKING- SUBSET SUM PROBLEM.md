![image](https://github.com/user-attachments/assets/9d5ab471-7e44-4058-b996-7bd4858ba745)# EX 2C BACKTRACKING- SUBSET SUM PROBLEM
## DATE:
## AIM:
To demonstrate that the sum of the subset of a given set is equal to the given sum.


## Algorithm
1. Take an integer input `n` representing the number of elements in the list.  
2. Read `n` integers from the user and store them in the list `arr`.  
3. Take an integer input `x` which is the target sum.  
4. Define a function `subsetSum` that takes `n`, `arr`, and `x` as parameters.  
5. In the function, iterate `i` from 0 to `n` to generate all possible subset sizes.  
6. For each size `i`, generate all combinations of `arr` of length `i` using `combinations(arr, i)`.  
7. For each subset generated, check if the sum of its elements is equal to `x`.  
8. If the sum matches `x`, print the subset as a list.  
9. Call the `subsetSum` function with the input values to find and display all matching subsets.  

## Program:
```
/*
Program to implement Subset sum problem.
Developed by: 
Register Number:  
*/
```
```PY
def SubsetSum(a,i,sum,target,n):
    if i==n:
        return sum==target
    if sum>target:
        return False
    if sum==target:
        return True
    return SubsetSum(a,i+1,sum,target,n) or SubsetSum(a,i+1,sum+a[i],target,n)

a=[]
size=int(input())
for i in range(size):
    x=int(input())
    a.append(x)

target=int(input())
n=len(a)
if(SubsetSum(a,0,0,target,n)==True):
    for i in range(size):
        print(a[i])
    print("True,subset found")
else:
    for i in range(size):
        print(a[i])
    print("False,subset not found")


```
## Output:

![image](https://github.com/user-attachments/assets/261e25e9-791c-484b-98e4-a3037400fb8c)

## Result:
The Subset Sum program executed successfully, and the result was determined based on whether a subset matching the target sum was found or not.
