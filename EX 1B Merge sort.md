# EX 1B Merge Sort
## DATE: 
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1. If the array has more than one element, split it into two halves.
2. Recursively apply merge sort on both halves.
3. Compare elements of both halves and merge them into a sorted array.
4. Copy any remaining elements from the left or right half.
5. Return the fully sorted array.
## Program:

/*
Program to implement Merge Sort
Developed by: Tharun.K
Register Number:  212222040172
*/

```python
def mergesort(li):
    if len(li) > 1:
        mid = len(li) // 2
        a = li[:mid]
        b = li[mid:]

        mergesort(a)
        mergesort(b)

        i = j = k = 0

        while i < len(a) and j < len(b):
            if a[i] < b[j]:
                li[k] = a[i]
                i += 1
            else:
                li[k] = b[j]
                j += 1
            k += 1

        while i < len(a):
            li[k] = a[i]
            i += 1
            k += 1

        while j < len(b):
            li[k] = b[j]
            j += 1
            k += 1
    
    if len(li) == n:
        mid = len(li) // 2
        
        for i in range(mid):
            print(li[i], end=" ")

      

li = []
m = []
n = int(input())  
for _ in range(n):
    a = int(input())
    li.append(a)
    m.append(a)

print("Given array is")
print(*li)  
print("\nSorted array is")
mid = len(li)//2
mergesort(li) 
for i in range(0,mid):
    print(m[i], end=" ")
```


## Output:
![Screenshot 2025-04-26 103457](https://github.com/user-attachments/assets/4920251d-54b9-4377-bf5a-008c4dd5c3d5)
## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
