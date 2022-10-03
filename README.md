{\rtf1\ansi\ansicpg1251\cocoartf2580
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 HelveticaNeue;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 1.1\
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardirnatural\partightenfactor0

\f1\fs26 \cf0 def areacalculator():\
    _input_ = input("enter the shape you want to calculate area of: ")\
    area = 0\
    p = 3.14\
    if _input_ == "square":\
        side = int(input("enter the value of side: "))\
        area = area + (side ** 2)\
    elif _input_ == "circle":\
        r = int(input("enter the value of r: "))\
        area = area + (2 * p * r)\
    elif _input_ == "rectangle":\
        length = int(input("enter the value of length: "))\
        width = int(input("enter the value of length: "))\
        area = area + (length * width)\
    elif _input_ == "triangle":\
        base = int(input("enter the value of base: "))\
        height = int(input("enter the value of height: "))\
        area = area +(0.5 * base * height)\
    else:\
        print("select a valid shape")\
    print("%.2f" % area)\
\
areacalculator()\
1.2\
import math\
def mean(arr):\
    mean = 0\
    sum = 0\
    for i in range(len(arr)):\
        mean += (arr[i]/len(arr))\
        sum += arr[i]\
    print(sum, ',', round(mean, 3))\
\
a = [15, 25, 21, 64, 34, 97, 84, 61]\
b = [54, 0, 31, 74, 89, 9, 0]\
c = [52, 40, 49, 94, 3, 70, 69, 4, 35, 21, 5]\
mean(a)\
mean(b)\
mean(c)\
2.1\
\
\
import math\
\
\
def hexagon(side):\
    return 6 * areaTriangle(side)\
\
\
def areaTriangle(side):\
    return (math.sqrt(3) / 4) * math.pow(5, 2)\
\
\
n = float(input("enter the side: "))\
\
print("%.2f" % hexagon(n))\
2.2\
def area(a, b):\
    area = a*b\
    print(area)\
\
a = int(input('The lenght of the first side of first rectangle: '))\
b = int(input('The lenght of the second side of first rectangle: '))\
area(a, b)\
a1 = int(input('The lenght of the first side of first rectangle: '))\
b1 = int(input('The lenght of the second side of first rectangle: '))\
area(a1, b1)\
a2 = int(input('The lenght of the first side of first rectangle: '))\
b2 = int(input('The lenght of the second side of first rectangle: '))\
area(a2, b2)\
3.1\
import math\
def cPow(lst):\
    h1 = math.sqrt(math.pow(lst[0],2)+math.pow(lst[1],2))\
    h2 = math.sqrt(math.pow(lst[2],2)+math.pow(lst[3],2))\
    print("hypotenuses of 1 triangle =",h1)\
    print("hypotenuses of 2 triangle =",h2)\
    if h1 > h2:\
        print("the hypotenus or 1st triangle largest:",h2)\
    elif h1 == h2:\
        print("they are equal")\
    else:\
        print("the hypotenus or 2nd triangle largest:",h2)\
\
tr=[]\
print("enter the sides of triangle")\
for i in range(2):\
    print("for",i+1,"triangle")\
    tr.append(float(input("the 1st side: ")))\
    tr.append(float(input("the 2st side: ")))\
\
cPow(tr)import math\
def cPow(lst):\
    h1 = math.sqrt(math.pow(lst[0],2)+math.pow(lst[1],2))\
    h2 = math.sqrt(math.pow(lst[2],2)+math.pow(lst[3],2))\
    print("hypotenuses of 1 triangle =",h1)\
    print("hypotenuses of 2 triangle =",h2)\
    if h1 > h2:\
        print("the hypotenus or 1st triangle largest:",h2)\
    elif h1 == h2:\
        print("they are equal")\
    else:\
        print("the hypotenus or 2nd triangle largest:",h2)\
\
tr=[]\
print("enter the sides of triangle")\
for i in range(2):\
    print("for",i+1,"triangle")\
    tr.append(float(input("the 1st side: ")))\
    tr.append(float(input("the 2st side: ")))\
\
cPow(tr)\
3.2\
\
\
def sort(str):\
    return ''.join(sorted(str))\
\
a = str(input('Enter the string: '))\
print (sort(a))\
4.1\
import math\
\
\
def divide(lst):\
    list_new1 = list(map(int, arr[0].split('/')))\
    list_new2 = list(map(int, arr[1].split('/')))\
    return reduceF([list_new1[0] * list_new2[1], list_new1[1] * list_new2[0]])\
\
\
def reduceF(lst):\
    divider, x, y = gcdEuclid(lst[0], lst[1])\
    return [i / divider for i in lst]\
\
\
def gcdEuclid(a, b):\
    if a == 0:\
        return b, 0, 1\
\
    gcd, x1, y1 = gcdEuclid(b % a, a)\
    x = y1 - (b // a) * x1\
    y = x1\
\
    return gcd, x, y\
\
\
arr = []\
for i in range(2):\
    arr.append(input("enter the fraction n" + str(i + 1) + ": "))\
result = divide(arr)\
print(result[0], "/", result[1])\
4.2\
def isInside(x, y, rad, p1, p2):\
    if ((p1 - x) * (p1 - x) +\
            (p2 - y) * (p2 - y) <= rad * rad):\
        return True\
    else:\
        return False\
p1 = 11\
p2 = 12\
x = 0\
y = 1\
rad = 2\
if isInside(x, y, rad, p1, p2):\
    print("Inside")\
else:\
    print("Outside")\
5.1\
import math\
\
import numpy\
\
\
def substract(lst):\
    list_new1 = list(map(int, arr[0].split('/')))\
    list_new2 = list(map(int, arr[1].split('/')))\
    result = [((numpy.lcm(list_new1[1], list_new2[1]) / list_new1[1]) * list_new1[0]) - (\
            (numpy.lcm(list_new1[1], list_new2[1]) / list_new2[1]) * list_new2[0]),\
              numpy.lcm(list_new1[1], list_new2[1])]\
\
    if (result[0] == 0):\
        print(result[0])\
    else:\
        print(result[0], "/", result[1])\
\
\
def reduceF(lst):\
    divider, x, y = gcdEuclid(lst[0], lst[1])\
    return [i / divider for i in lst]\
\
\
def gcdEuclid(a, b):\
    if a == 0:\
        return b, 0, 1\
\
    gcd, x1, y1 = gcdEuclid(b % a, a)\
    x = y1 - (b // a) * x1\
    y = x1\
\
    return gcd, x, y\
\
\
arr = []\
for i in range(2):\
    arr.append(input("enter the fraction n" + str(i + 1) + ": "))\
substract(arr)\
5.2\
def printt(a):\
    for i in a:\
        print(i, end=', ')\
\
def division(a):\
    b = []\
    for i in range(1, (a+1)):\
        if a%i==0:\
            b.append(i)\
    printt(b)\
\
\
a = int(input('Enter the number: '))\
division(a)\
6.1\
def gcdEuclid(a, b):\
    if a == 0:\
        return b, 0, 1\
\
    gcd, x1, y1 = gcdEuclid(b % a, a)\
    x = y1 - (b // a) * x1\
    y = x1\
\
    return gcd, x, y\
\
\
def lcm(a, b):\
    gcd, x, y = gcdEuclid(a, b)\
    return (a * b) / gcd\
\
\
a, b = list(map(int, input("enter a,b: ").split()))\
gcd, x, y = gcdEuclid(a, b)\
print("GCD is:", gcd)\
print("LCM is:", lcm(a, b))\
6.2\
import math\
\
\
def quadrilateralArea(lst, diagonal):\
    h1 = 2 * (areaTriangle(lst[0], lst[1], diagonal) / diagonal)\
    h2 = 2 * (areaTriangle(lst[2], lst[3], diagonal) / diagonal)\
    area = 0.5 * diagonal * (h1 + h2)\
    return area\
\
\
def areaTriangle(a, b, c):\
    s = (a + b + c) / 2\
    area = math.sqrt(s * (s - a) * (s - b) * (s - c))\
    return area\
\
\
x = list(map(float, input("enter 4 sides one after one: ").split()))\
d = float(input("enter the diagonal: "))\
print("area of quadrilateral: ", quadrilateralArea(x, d))\
7.1\
import math\
\
\
def quadrilateralArea(lst):\
    s = (lst[0] + lst[1] + lst[2] + lst[3]) / 2\
    area = math.sqrt(((s - lst[0]) * (s - lst[1]) * (s - lst[2]) * (s - lst[3])) - (\
                lst[0] * lst[1] * lst[2] * lst[3] * math.pow(math.cos(math.pi / 2), 2)))\
    return area\
\
\
x = list(map(int, input("enter 4 sides one after one: ").split()))\
print("area of quadrilateral: ", quadrilateralArea(x))a\
7.2\
def occt(a):\
    if a > 0:\
        return oct(a)\
    else:\
        return 'There is no way.'\
\
a = int(input('Enter the number: '))\
print(oct(a))\
8.1\
def division(n):\
    for i in range(n):\
        if divide(i) == True:\
            print(i)\
\
\
def divide(n):\
    temp = n\
    while (temp > 0):\
\
        digit = temp % 10\
        if ((digit != 0 and n % digit == 0) == False):\
            return False\
\
        temp = temp // 10\
\
    return True\
\
\
n = int(input("enter the numb: "))\
division(n)\
8.2\
def swap(lst):\
    lst[0],lst[len(lst)-1] = lst[len(lst)-1],lst[0]\
    return lst\
input("the length of array: ")\
list_new = list(map(int, (input("Enter the array: ")).split()))\
print("original array: ",list_new)\
print("swapped: ",swap(list_new))\
9.1\
def Sum(n):\
    sum = 0\
    for digit in str(n):\
        sum += int(digit)\
    return sum\
\
\
def sumC(n, sum):\
    repeat = -1\
    while n >= 0:\
        n -= sum\
        repeat += 1\
    return repeat\
\
\
n = int(input("Enter the number: "))\
sum = Sum(n)\
print(sum)\
print(sumC(n, sum))\
9.2\
import statistics\
\
def multiplyList(myList):\
\
	result = 1\
	for x in myList:\
		result = result * x\
	return result\
\
\
list1 = [1, 2, 3]\
list2 = [4, 5, 6]\
list3 = [7, 8, 9]\
\
print("The product of the elements in 1 list =", multiplyList(list1))\
print("The product of the elements in 2 list =", multiplyList(list2))\
print("The product of the elements in 3 list =", multiplyList(list3))\
\
print("The arithmetic mean of 1 list =", statistics.mean(list1))\
print("The arithmetic mean of 2 list =", statistics.mean(list2))\
print("The arithmetic mean of 3 list =", statistics.mean(list3))\
10.1\
\
\
interval = []\
for i in range(210, 231):\
    interval.append(i)\
\
res = [sub for sub in interval if len(set(str(sub))) == len(str(sub))]\
\
print(str(res))\
10.2\
string = input("enter the str: ")\
s = string.split()[::-1]\
w = []\
for i in s:\
    w.append(i)\
print(" ".join(w))\
11.1\
def isPrime(n):\
    if n <= 1:\
        return False\
    for i in range(3, n):\
        if n % i == 0:\
            return False\
    return True\
\
def print(n):\
    for i in range(n, n * 2):\
        if isPrime(i):\
            print(i, end=" ")\
\
n = int(input("enter the n: "))\
print(n)\
11.2\
list1 = [10, 250, 20, 4, 100, 45, 99]\
\
print(list1)\
print("maximum of 1st list:", max(list1))\
\
list2 = [15, 86, 54, 320, 112, 55, 74]\
\
print(list2)\
print("maximum of 2nd list:", max(list2))\
\
index1 = list1.index(max(list1))\
index2 = list1.index(max(list2))\
\
list1[index1], list2[index2] = list2[index2], list1[index1]\
\
print(list1, list2)\
12.1\
def findFriendly(n):\
    f = 0\
    for ch in range(n):\
        if ch != f:\
            s1 = 0\
            for i in range(1, ch // 2 + 1):\
                if ch % i == 0:\
                    s1 += i\
            s2 = 0\
            for j in range(1, s1 // 2 + 1):\
                if s1 % j == 0:\
                    s2 += j\
            if s2 == ch != s1:\
                print(ch, s1)\
                f = s1\
\
\
n = int(input("enter the numb: "))\
findFriendly(n)\
12.2\
import math\
\
def median(a, b, c):\
    median = math.sqrt(2 * (b * b + c * c) - a * a) / 2\
    return median\
\
print("enter 3 sides:")\
a = int(input("a = "))\
b = int(input("b = "))\
c = int(input("c = "))\
if abs(a - b) >= c | a + b <= c:\
    print("impossible triangle")\
print("medians of original triangle:")\
mA = median(a, b, c)\
mB = median(b, a, c)\
mB = median(c, a, b)\
print(ma, mb, mc)\
print("medians of created triangle:")\
mmA = median(mA, mB, mB)\
mmB = median(mB, mA, mC)\
mmC = median(mC, mA, mB)\
print(mmA, mmB, mmC)\
Footer\
\'a9 2022 GitHub, Inc.\
Footer navigation\
13.1\
def armStrong(n):\
    for num in range(1, 1000):\
        order = len(str(num))\
        sum = 0\
        a = num\
        while a > 0:\
            digit = a % 10\
            sum += digit ** order\
            a //= 10\
\
        if num == sum:\
            print(num)\
\
\
n = int(input("enter the n: "))\
armStrong(n)\
13.2\
def acos(x, y):\
    return x / ((x * x + y * y) ** 0.5)\
\
x1, x2 = map(float, input().split())\
y1, y2 = map(float, input().split())\
z1, z2 = map(float, input().split())\
\
res = [x1, x2]\
acosx = acos(x1, x2)\
acosy = acos(y1, y2)\
\
if acosy > acosx:\
    acosx = acosy\
    res = [y1, y2]\
acosz = acos(z1, z2)\
if acosz > acosx:\
    acosz = acosz\
    res = [z1, z2]\
    \
print(*res)\
n = 3\
res = [tuple(map(float, input().split())) for i in range(n)]\
rcos = [acos(*res[i]) for i in range(n)]\
k = rcos.index(max(rcos))\
print(res[k])\
14.1\
def countDivisors(a):\
    result = []\
    i = 1\
    while i * i < a + 1:\
        if a % i == 0:\
            result.append(i)\
            if i != a // i:\
                result.append(a // i)\
        i += 1\
    return sorted(result)\
\
\
def function(m, n):\
    div = []\
    for num in range(m, n + 1):\
        frac = countDivisors(num)\
        div.append((len(frac), -num, frac[-2:]))\
    div.sort()\
    print(-div[-1][1], 'consist', div[-1][0], 'divisors')\
\
\
function(2, 4682192)\
14.2\
import math\
def distance(a, b):\
    d = 0\
    for i in range(2):\
        d += pow((a[i] - b[i]), 2)\
    return d\
Identify = ['X', 'Y', 'Z', 'T']\
arr = []\
print("enter the coordinates:")\
for i in range(4):\
    b = []\
    print("coordinates:", Identify[i])\
    for j in range(2):\
        b.append(int(input()))\
    arr.append(b)\
flag = True\
for i in range(2):\
    for j in range(i + 1, 4):\
        dist = distance(arr[i], arr[j])\
        if flag or max_dist < dist:\
            m1 = i\
            m2 = j\
            max_dist = dist\
            flag = False\
print(f'maximum distance from each other: \{Identify[m1]\} \uc0\u1080  \{Identify[m2]\}')\
print(f'value of this distance:  \{max_dist ** 0.5:.3f\}')\
15.1\
def findPrime(n):\
    arr = [True for _ in range(n + 1)]\
    i = 1\
    while 2 * i * (i + 1) < n:\
        j = i\
        while j <= (n - i) / (2 * i + 1):\
            arr[2 * i * j + i + j] = False\
            j = j + 1\
        i = i + 1\
    for i in range(1, n + 1):\
        elem = arr[i]\
        if elem:\
            prime = 2 * i + 1\
            if prime > n: break\
            a = bin(prime)[2:]\
            b = bin(prime)[2:][::-1]\
            if a == b:\
                print(prime, end=' ')\
n = int(input("enter the numb: "))\
findPrime(n)\
15.2\
import math\
def distance(a, b):\
    d = 0\
    for i in range(3):\
        d += pow((a[i] - b[i]), 2)\
    return d\
Identify = ['X', 'Y', 'Z', 'T']\
arr = []\
print("enter the coordinates:")\
for i in range(4):\
    b = []\
    print("coordinates:", Identify[i])\
    for j in range(3):\
        b.append(int(input()))\
    arr.append(b)\
flag = True\
for i in range(3):\
    for j in range(i + 1, 4):\
        dist = distance(arr[i], arr[j])\
        if flag or min_dist > dist:\
            m1 = i\
            m2 = j\
            min_dist = dist\
            flag = False\
print(f'minimal distance from each other: \{Identify[m1]\} \uc0\u1080  \{Identify[m2]\}')\
print(f'value of this distance:  \{min_dist ** 0.5:.3f\}')}
