def max_attain(a):
    if len(a) == 2:
        return max(a)
    if len(a) == 1:
        return a[0]
    if len(a) == 3:
        return max(a[1], a[0] + max_attain(a[2:]))
    return max(a[1] + max_attain(a[3:]), a[0] + max_attain(a[2:]))
n=int(input("Enter number of houses: "))
a=[]
for i in range(n):
    c=int(input("Enter value: "))
    a.append(c)
print("Max stolen: ",max_attain(a))