# DSA-assignment

ASIGNMENT 1
1/
def mergeSort(arr, low, high): 
 if low < high: 
 mid = (low + high) // 2 
 mergeSort(arr, low, mid) 
 mergeSort(arr, mid + 1, high) 
 merge(arr, low, mid, high) 
def merge(arr, low, mid, high): 
 temp = [] 
 left = low 
 right = mid + 1 
 while left <= mid and right <= high: 
 if arr[left] < arr[right]: 
 temp.append(arr[left]) 
 left += 1 
 else: 
 temp.append(arr[right]) 
 right += 1 
 while left <= mid: 
 temp.append(arr[left]) 
 left += 1 
 while right <= high: 
 temp.append(arr[right]) 
 right += 1 
 for i in range(low, high + 1): 
 arr[i] = temp[i - low] 
arr = [12, 11, 13, 5, 6, 7] 
mergeSort(arr, 0, len(arr) - 1) 
print(arr)

2/
def selection_sort(arr): 
 n = len(arr) 
 for i in range(n-1): 
 mini = i 
 for j in range(i, n): 
 if arr[j] < arr[mini]: 
 mini = j 
 arr[i], arr[mini] = arr[mini], arr[i] 
 print(arr) 
# Main 
arr = [64, 25, 12, 22, 11] 
selection_sort(arr) 


def insertionSort(arr): 
 for i in range(1, len(arr)): 
 key = arr[i] 
 j = i-1 
 while j >=0 and key < arr[j] : 
 arr[j + 1] = arr[j] 
 j -= 1 
 arr[j + 1] = key 
 return arr 
#Main 
arr = [12, 11, 13, 5, 6] 
print(insertionSort(arr))


ASSIGNMENT 2
1/
def binary_search(arr, target): 
 start = 0 
 end = len(arr) - 1 
 
 while start <= end: 
 mid = start + (end - start) // 2 
 if arr[mid] == target: 
 return mid 
 elif arr[mid] < target: 
 start = mid + 1 
 else: 
 end = mid - 1 
 
 return -1 
# Example usage 
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
target = 5 
result = binary_search(arr, target) 
if result != -1: 
 print(f"Element found at index {result}") 
else: 
 print("Element not found")


 2/
 def linear_search(arr, target): 
 for i in range(len(arr)): 
 if arr[i] == target: 
 return True 
 return False 
arr = [5,9,4,1,2,7,3,8] 
target = 7 
if linear_search(arr, target): 
 print("Element found") 
else: 
 print("Element not found")


 


