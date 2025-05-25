# EX 4D DYNAMIC PROGRAMMING – 4
## DATE:
## AIM:
To find the minimum number of operations to convert str1 to str2 using Naive recursive method.


## Algorithm
1. If one string is empty, return the length of the other string.
2. If the last characters of both strings match, the cost is 0; else, cost is 1.
3. Recursively calculate three options: insert, delete, or replace a character.
4. Take the minimum of the three operations plus the current cost.
5. Final result is the minimum number of edits needed to convert one string into another.  

## Program:
```
Developed by: SAKTHIVEL R
Register Number: 212222100044
```
```py
def LD(s, t):
    
    if s == "":
        return len(t)
    if t == "":
        return len(s)
    if s[-1] == t[-1]:
        cost = 0
    else:
        cost = 1
    res = min([LD(s[:-1], t)+1, LD(s, t[:-1])+1, LD(s[:-1], t[:-1]) + cost])
    return res
str1=input()
str2=input()
print('Edit Distance',LD(str1,str2))
```

## Output:

![22d](https://github.com/user-attachments/assets/c0950bc0-fc03-4f3c-956a-5b6b72110bb9)



## Result:

Thus the program was executed successfully for finding edit distance between two strings.
