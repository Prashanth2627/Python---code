# Python---code

### Program 1
### Ouestion:
A college maintains the daily attendance details of its students in the form of a list containing student IDs. Some students may have attended multiple sessions on the same day. The administration wants to identify the longest continuous sequence of sessions in which no student ID is repeated. Develop a solution that determines the maximum length of such a sequence. 

### Program
```
arr = [1,2,3,1,4]

max_len = 0

for i in range(len(arr)):
  unique = []

  for j in range(1,len(arr)):
    if arr[j] in unique:
      break

    unique.append(arr[j])

  if len(unique) > max_len:
    max_len = len(unique)

print(max_len)

```
### Output:
<img width="1917" height="642" alt="image" src="https://github.com/user-attachments/assets/8f8f0db8-54dd-475d-813f-5ca39d36652a" />

### Program 2:
### Question:
An online shopping application stores the prices of products viewed by a customer during a browsing session. The customer wants to identify a continuous range of products that provides the maximum possible total discount value. Given the discount values, determine the maximum value that can be obtained from any continuous range. 

### Program
```
arr = [-2,3,4,-1,2]

max_sum = 0

for i in range(len(arr)):
  tot = 0

  for j in range(1,len(arr)):
    tot = tot + arr[j]

    if tot > max_sum:
      max_sum = tot

print(max_sum)

```

### Output:
<img width="1910" height="807" alt="image" src="https://github.com/user-attachments/assets/07bcbb30-d684-44b5-ba83-060a5255f765" />


### Program 3:
### Question:
A city installs buildings of different heights along a straight road. During rainfall, water gets collected between taller buildings. The engineering team needs to calculate the total amount of water that can remain trapped after heavy rainfall based on the heights of the buildings. 

### Program:
```
height = [0, 1, 0, 2, 1, 0]

water = 0

for i in range(len(height)):
    left_max = 0
    right_max = 0

    for j in range(i + 1):
        if height[j] > left_max:
            left_max = height[j]

    for j in range(i, len(height)):
        if height[j] > right_max:
            right_max = height[j]

    if left_max < right_max:
        water += left_max - height[i]
    else:
        water += right_max - height[i]

print(water)

```

### Output:
<img width="1655" height="627" alt="image" src="https://github.com/user-attachments/assets/37ee4057-8405-461c-8647-c78888f24bfb" />


### Program 4:
### Question:
A company stores the monthly performance scores of an employee for several months. The scores may contain both positive and negative values depending on the employee's performance. Management wants to identify the continuous period during which the employee achieved the highest overall performance. 


### Program
```
arr = [-2,5,-1,3,-4]

max_sum = 0

for i in range(len(arr)):
  tot = 0

  for j in range(1,len(arr)):
    tot = tot + arr[j]

    if tot > max_sum:
      max_sum = tot

print(max_sum)

```

### Output
<img width="1912" height="727" alt="image" src="https://github.com/user-attachments/assets/8a002899-d960-42a4-b7bd-313f3bcd0f5c" />


### Program 5:
### Question
A retail company stores the daily sales quantity of a product for several consecutive days. Due to seasonal changes, some days may have negative adjustments. The company wants to identify the period that produced the highest multiplication of sales-related values. Develop a solution to determine this maximum product. 

### Program
```
arr=[-2,3,-4]
max_pro = arr[0]

for i in range(len(arr)):
  product = 1

  for j in range(i,len(arr)):
    product = product * arr[j]

  if product > max_pro:
    max_pro = product

print(max_pro)
```
### Output:
<img width="1917" height="652" alt="image" src="https://github.com/user-attachments/assets/86aed232-aaaa-4b69-af2c-3c85d78132b7" />

### Program 6:
### Question
An e-commerce application stores the product IDs purchased by a customer in chronological order. The same product may appear multiple times. The system needs to determine the longest sequence of consecutive purchases in which every product ID is unique.

### Program:
```
arr = [1,2,3,1,4]

max_len = 0

for i in range(len(arr)):
  unique = []

  for j in range(1,len(arr)):
    if arr[j] in unique:
      break

    unique.append(arr[j])

  if len(unique) > max_len:
    max_len = len(unique)

print(max_len)

```
### Output:
<img width="1752" height="635" alt="image" src="https://github.com/user-attachments/assets/ae282aa6-1064-40ae-b8dd-5acf44cbd365" />

### Program 7:
### Question
A bank stores transaction amounts for a customer's account. A continuous group of transactions may add up to a specific target amount. The auditing system needs to determine how many different continuous transaction groups produce exactly the specified amount. 

### Program:
```
arr=[1,2,3,2]
target = 5
count=0

for i in range(len(arr)):
  total = 0

  for j in range(i,len(arr)):

    total = total + arr[j]

    if total == target :
      count = count + 1

print(count)
```

### Output:
<img width="1872" height="573" alt="image" src="https://github.com/user-attachments/assets/06421876-50f0-4643-9e4d-40d798ed6549" />

### Program 8 :
### Question
A company receives a list of employee skill codes represented as strings. Employees having the same set of characters in their skill codes belong to the same skill category, even if the characters appear in a different order. The HR system needs to organize employees into appropriate skill groups. 

### Program:
```
words=["eat","tea","tan","ate","nat","bat"]

groups= {}

for word in words:
  letters = list(word)
  letters.sort()

  key="".join(letters)

  if key not in groups:
    groups[key]=[]

  groups[key].append(word)

for group in groups.values():
  print(group)

```

### Output:
<img width="1912" height="602" alt="image" src="https://github.com/user-attachments/assets/e361122a-5701-43fe-95a4-e7fa80bdd66a" />

### Program 9:
### Question
A network monitoring system receives packet identifiers in chronological order. The system must determine the longest sequence of consecutive packets whose identifiers form a continuous numerical sequence, regardless of their original order in the incoming data. 

### Program:
```
arr = [100,4,200,1,2,3]

arr.sort()

count = 1
max_count = 1

for i in range(1,len(arr)):
  if arr[i]==arr[i-1]+1:
    count+=1
  elif arr[i]!=arr[i-1]+1:
    count = 1

  if count > max_count :
    max_count = count
print(max_count)

```

### Output:
<img width="1837" height="623" alt="image" src="https://github.com/user-attachments/assets/191c825a-6f43-4fb3-98b3-f16a9e3048cf" />


### Program 10:
### Question:
A hospital receives appointment requests represented by starting and ending times. Some appointments overlap with each other. The scheduling system needs to combine overlapping appointment periods so that the final schedule contains only non-overlapping time ranges. 

### Program:
```
arrs=[[1, 3], [2, 6], [8, 10], [9, 12]]
arrs.sort()
result=[]

for arr in arrs:
  if not result or arr[0]>result[-1][1]:
    result.append(arr)
  else:
    result[-1][1]=max(result[-1][1],arr[1])

print(result)

```

### Output:
<img width="1571" height="681" alt="image" src="https://github.com/user-attachments/assets/3bbec38b-23e8-40a0-a598-425239394191" />







