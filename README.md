# MATRIX-PATTERN
n=int(input("enter the size:"))
matrix=[[0]*n for _ in range(n)]
top,left=0,0
right,bottom=n-1,n-1
num=1
while top<bottom and left<=right:
    for i in range(left,right+1):
        matrix[top][i]=num
        num+=1
    top+=1
    for i in range(top,bottom+1):
        matrix[i][right]=num
        num+=1
    right-=1
    for i in range(right,left-1,-1):
        matrix[bottom][i]=num
        num+=1
    bottom-=1
    for i in range(bottom,top-1,-1):
        matrix[i][left]=num
        num+=1
    left+=1
for row in matrix:
    for val in row:
        print(f"{val:3}",end='')
    print()
OUTPUT:
enter the size: 6
  1  2  3  4  5  6
 20 21 22 23 24  7
 19 32 33 34 25  8
 18 31 36 35 26  9
 17 30 29 28 27 10
 16 15 14 13 12 11

n=int(input("enter the size:"))
matrix=[['']*n for _ in range(n)]
top,left=0,0
right,bottom=n-1,n-1
num=0
while top<=bottom and left<=right:
    for i in range(left,right+1):
        matrix[top][i]=chr(65 + num % 26)
        num+=1
    top+=1
    for i in range(top,bottom+1):
        matrix[i][right]=chr(65 + num % 26)
        num+=1
    right-=1
    for i in range(right,left-1,-1):
        matrix[bottom][i]=chr(65 + num % 26)
        num+=1
    bottom-=1
    for i in range(bottom,top-1,-1):
        matrix[i][left]=chr(65 + num % 26)
        num+=1
    left+=1
    
for row in matrix:
    for val in row:
        print(f"{val:3}",end='')
    print()
    OUTPUT:
    enter the size: 5
A  B  C  D  E  
P  Q  R  S  F  
O  X  Y  T  G  
N  W  V  U  H  
M  L  K  J  I 
