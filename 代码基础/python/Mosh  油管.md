
IDE == integrated development environment

the python code ecxcute line by line 

# Print 打印

In quatations, we define a string == a series of characters

``` python
print("*" * 10)
```

# Variables

pytthon will allocate some memory 
```python
price = 10  
price = 20
print(price) # no quatation because of value
```

Will store the "10" in the memory, then attach the "price" label in  that memory location.
Python interpreter excutes code from top. Reset as 20.

``` python
rating = 4.9 # floating number (floats)
name = 'HELLO'  # strings
is_published = True  
# underscore to separate multiple words.
# True or Flase -- Boolean value
# python对大小写敏感，true这个就是错误的布尔值，必须是True
# vaiables - lowercase letter
i_published = False
```
### execise 
![[mosh_1.png]]
设定三个变量
```python
name = "John Smith"
age = 20
is_new = True
```
How to receive input from the user

`input('What is your name? ')`会在terminal中让输入，可以定义如`name = input('What is your name? ')`  

==julia 中没有input函数， 而是利用`readlines()`，但是可以自己定义==
```julia
function input(prompt::String="")::String
    print(prompt)
    return chomp(readline())
end
x = parse(Int, input());
```

``` python
patient_name = 'John Smith'
patient_age = 20
patient_status = 'New'
patient_status_plus = True
is_new = True
# name = input('What is your name? ')

name = input('What is your name? ')
color = input('What is your favorite color? ')
print('Hi ' + name)
print(name + ' likes ' + color + '.')
```
# Type Conversion

``` python
birth_year = input('Birth year: ')
# input函数，无论你在终端输入什么，都会被认为是字符串类型的 Strings
# 2020 - ‘1999’  -- ERROR
# 用函数是强制转换类型
# int() float() bool()
# 获得变量的类型，并打印类型的函数 type()函数获取括号内变量的数据类型
print(type(birth_year)) # 得到 String <class 'str'>
age = 2024 - int(birth_year)
print(type(age)) # <class 'int'>
print(age)
```
### exercise
![[mosh_2.png]]

```python
weight_lbs = input('What your weight in pounds？ ')
weight_kg = int(weight_lbs) * 0.45
print(weight_kg)
print(str(weight_kg) + 'kg')
```
## Strings
==单双引号区别== 
apostrophe n.撇号；单引号
``` python
course = 'Python's Course for Beginners' 
```


这句会报错，因为在''s之前字符串就结束了
运用**双引号 “ ”**

``` python
course = "Python's Course for Beginners"
print(course)
# 同样单引号也有这种用法
course = 'Python for "Beginners"'
print(course)
```
use triple quate to define a multiple lengths

```python
course = '''
Hi John

Here is our first email to you.

Thank you,
The support team
'''
print(course)
```
## Index
```python
course = 'Python for Beginners'
#         012
print(course[0])  # “索引，在其它编程语言中没有的特性之一”  P
print(course[-1])   # s  negative index strat from the end
print(course[-2])   # r
print(course[0:3])  # 从0到3 Pyt
print(course[0:])   # Python for Beginners
print(course[1:])   # ython for Beginners
print(course[:5])   # Pytho

# copy [:]
course = 'Python for Beginners'
another = course[:]  # 得到整个长度的字符串
print(another) # 得到Python for Beginners 

```

```PYTHON
name = 'Jennifer'
print(name[1:-1]) # ennife 从第二个到倒数第一个
```

>python 的从0开始索引真的反直觉，发明意大利楼层的一定是个python。
 ==python 从0开始索引，julia从1开始索引。==
## Formatted strings
``` python
first = 'John'
last = 'Smith'
message = first + '[' + last + ']' is a coder
print(message)
```

hard to visulize the output
use curly braces `{}`  to dynamically insert values into strings
`f`   format sting

```python
msg = f'{first} [{last}] is a coder'
print(msg)
```

## String method

```python
course = 'Python for Beginners'
print(len(course))
print(course.upper())
print(course.lower())

print(course.find('P'))
print(course.find('o')) #4
print(course.find('O')) #-1 没有O
print(course.replace('Beginners') # 11 Beginners 从11 开始

print(course.replace('Beginners', 'Absolute Beginners'))
print(course.replace('P', 'J'))

# in operater "..." in varibles
print('Python' in course) # True， 存在于变量中
print('python' in course) # False
```
*Differenece between methods and functions*
function specific to strings are methods.
Or a function belongs to something else or specific to some objects.------- refer to as methods.
`print()`,`len()` are function

# Arithmetic

```python
print(10 // 3)  # 3  整除
print(10 / 3)   # 3.33333333
print(10 % 3)   # 1
print(10 ** 3)  # 10^3  exponent
```

 
### Augmented assignment operator

`x +`  是一种简便写法， +可以任意替换
```python
x = 10
x = x + 3 # result is 13 and then restore in x 
x += 3 
```

### Operator Precedence

Actually, all the programming language behave the same way.

parenthesis
exponentiation  `2 ** 3`
multiplication or division
addition or subtraction

## Math function

```python
x = 2.9
print(round(x))  #1.51以上取 2 ， 包括1.5一下取1.
print(abs(-2.9))  # 取绝对值 absolute
```

### math module

 A module in Python is a separate file with some reusable code.
 
``` python
import math  # import 要放在最上方
# Search : Python 3 math model, then you could see the file about it.

print(math.ceil(2.9))  
print(math.floor(2.9)) 
```

# If Statements
 allow to build programs that can make decisions based on some condition.

定义if后 下一行会自动对其
用shift & tab， 光标回到这条线的开始处

``` python
is_hot = False # 定义为布尔值
is_cold = False
if is_hot:
    print("It's a hot day")
    print("Drink plenty of water")
elif is_cold:
    print("It's a cold day")
    print("Wear warm clothes")
else:
    print("It's a lovely day")
print("Enjoy your day")
```
### exercise
![[mosh_3.png]]
``` python
house_price = 1000000  
has_good_credit = True
if good_credit:
    put_down = house_price * 0.1
else:
    put_down = house_price * 0.2
print(f'Their down payment is ${put_down}')
```
## Logical Operators

AND: both
OR: at least one
NOT: convert true boolean value to false
``` python
has_high_income = True
has_good_credit = True

if has_good_credit and has_high_income:
    print("Eligible for loan")  

# or condition 
has_high_income = True
has_good_credit = False

if has_good_credit or has_high_income:
    print("Eligible for loan")  

# Not condition
has_good_credit = True
has_criminal_record = False

if has_good_credit and not has_criminal_record:
    print("Eligible for loan")
```

对于一整段注释， 可以用 `ctrl + / ` 注释

## Comparision operators

``` python
temperature = 30
if temperature > 30:
    print("It's a hot day")
else:
    print("It's not a hot day")
```
会输出It's not a hot day， 30不大于30

也可也 `>=; <=; ==; !=`   
单等号是设置变量, 不是设置布尔值
```python
temperature = 35
if temperature >= 30:
    print("It's a hot day")
else:
    print("It's not a hot day")
```
### Exercise

```python
name = input("Please input your name ")
if len(name) < 3:
    print("name must be at least 3 characters")
elif len(name) > 50:
    print("name can be a maximum of 50 characters")
else:
    print("name looks good!")
```
### Weight Converter

```python
weight = input('Weight: ')
weight_unit = input('(L)bs or (K)g: ')
# if weight_unit == 'L' or weight_unit == 'l':
if weight_unit.upper() == 'L':  # 输入大小写都可以
    weight_kilo = int(weight) * 0.45
    print(f'You are {weight_kilo} kilos')
#    print('You are ' + str(weight_kilo) + ' kilos')
else:
    weight_pounds = int(weight) / 0.45
    print(f'You are {weight_pounds} pounds')
```
# While loop

use while loop to excute a block of code multiple times.

```python
i = 1
while i <= 5:
    print('*' * i)
    i = i + 1
print("Done")
```
## Guessing Game
```python
secret_number = 9
guess_count = 0
guess_limit = 3
while guess_count < guess_limit:  # while也有else的部分
    guess = int(input("Guess: "))
    guess_count += 1
    if guess == secret_number:
        print("You won!")
        break    # terminate our while loop
else:
    print("Sorry, you failed!")


```
使代码的可读性更高，可以不使用`i` 作为循环数量
为变量使用有意义和描述性的名称
![[mosh_rename.png]]
右键要修改的变量 refactor -> rename
或者快捷键 shift + F6
再把3改成guess_limit 使得代码的可读性更强
### Car Game
```python
shuru = input('>' )
while shuru.lower != 'quit':
    if  shuru.lower() == 'help':
        print( ' start - to star the car ')
        print( ' stop  - to stop the car ')
        print( ' quit  - to exit helo')
    elif shuru.lower() == 'start':
        print(' Car started, ready to go! ')
    elif shuru.lower() == 'stop':
        print(' Car stopped! ')
    else:
        print(" I don't understand ")
        break
    shuru = input('>' )
```
==自己写的出现的问题==
1. 经常忘记if 条件后的冒号。
2. 程序不完全正确，在输入quit以后，程序会结束，但是会打印出 I don‘t understand.  视频第一个范例解释了此错误。此`while循环`只负责了循环，而在if中只比较了不同的输入。在输入quit时会结束循环，但是也会带入if循环中得到 idu。
3. 忘记了三个引号或者双引号可以输入多重（有印象但是忘用了）

``` python
command = ""
while True:
    command = input('>').lower() 
    if command. == 'help':
        print('''
start - to start the car
stop - to stop the car
quit - to exit
                 ''')

    elif command == 'start':
        print("Car started...Ready to go!")

    elif command == 'stop':
        print("Car stopped.")
    elif command == 'quit': 
         break
    else:
        print("I don't understand that...")
```
==comment==
1. `command = ""` 设置为empty string
2. ` command = input('>').lower()` 可以避免太多次 `.lower()`,为了可读性尽量不要重复。
3. `"""三引号多行内容"""`会显示引号中间内容，输入了什么就是什么，会把前面的空格显示出来，需要删除。
4.  `while true `就是说一直循环，直到等于quit时候结束while 循环。
5. 如果输入两次一样的如两次start，会得到两次启动。如何改进？

==改进==
利用布尔值，在计算机内存中加入汽车启动与否的状态。

```python
# 加上started的代码，
command = ""
started = False
while True:  
    command = input("> ").lower()
    if command == "start":
        if started:
            print("Car is already started!")
        else:
            started = True
            print("Car started...")
    elif command == "stop":
        if not started:
            print("Car is already stopped!")
        else:
            started = False
            print("Car stopped.")
    elif command == "stop":
        print("Hi guys you had stopped it!")
    elif command == "help":  
        print("""
start - to start the car
stop - to stop the car
quit - to exit
        """)
    elif command == "quit": 
        break
    else:
        print("I don't understand that...")
```
# For Loops

==while loops:== excute a block of code multiple times.
==for loops:== iterate over items of a collection

``` python
for item in 'Python':
    print(item)
```

```  python
for item in ['Mosh', 'John', 'Sarah']:
    print(item)

for item in [1, 2, 3, 4]:
    print(item)

for item in range(10): 
    print(item) #    0到9，没有10

for item in range(5, 10):
    print(item) #5到9

for item in range(5, 10, 2):  #最后一个部分是step，range(5, 10)的范围内，以单位2走一步
    print(item) #5，7，9.
```
### exercise
calculate all the item in shopping cart.
``` python
#自己瞎写的
item = [10, 20, 30]
i = 1
final_cost = item[0]
while i <= 2:
    final_cost = final_cost + item[i]
    i = i + 1
print(final_cost)
```
==谁说站在while里的不算英雄==
其实暴露了不理解的时for循环的把所有项目迭代在一个集合的具体含义，迭代出来的所有结果并不是把行向量转置为列向量。

``` python
prices = [10, 20, 30]
total = 0
for price in prices:
    total += price
print(f'Total: {total}')
```
# Nested Loops 嵌套循环

``` python
for x in range(4):        #outer loop
    for y in range(3):    #inner loop
        print(f'({x}, {y})')
#会得到所有（x,y）的组合
```
先迭代inner loop，所以结果的前三个的x坐标没有变（x = 0）。inner loop完成迭代后，outer loop 再迭代一次（x = 1），再次全部迭代inner loop。

### exercise 
``` python
ori = 2
for y in range(1):
    for ite in [ +3 , 0, +3, 0, 0]:
        print((ori + ite) * 'x' )
```
 ==没有利用嵌套== 
 删去第一行仍然成立
 后面给了一个开头为`numbers = [5, 2, 5, 2, 2]` 再次尝试。

 同时在其他语言中不能直接用数字乘string。
 我们假设不能这样做，通过inner loop 解决。
 
``` python
numbers = [5, 2, 5, 2, 2]
for x_count in numbers:
    output = ""
    for result in range(x_count):
        output += 'x'
    print(output)
```
==重点在于理解 inner loop ==
`for result in range(x_count): `第一次内循环 循环`range(5)` 相当于叠加5次。

一些关于空字符的理解
```python
test = ""
print(test)
test = test + 'x'
print(test)
test = test + 'x' + 'x'
print(test)
```
# List

``` python
name = ['John', 'Bob', 'Mosh', 'Sarah', 'Mary']
print(name)
```
在terminal中会得到类似的`['John', 'Bob', 'Mosh', 'Sarah', 'Mary']`

## index in list

``` python
print(name[0]) 
print(name[2])
print(name[-1])
print(name[-2])
print(name[2:])   # [2:]是Mosh到Mary
print(name[2:4])  # [2:4]是Mosh到Sarah，因为这里结束索引是4，它会返回所有项到这个索引，但是不包括这个索引中的Mary
print(name[4])  # Mary
print(name[:4]) # 没有mary
print(name) # NOT AFFERCT
```

John的名字写错了，t替换
``` python
names = ['Jon', 'Bob', 'Mosh', 'Sarah', 'Mary']
names[0] = 'John'
print(names)
```

### exercise
 Write a program to find the largest number in a list
 ``` python
number_list = [15, 60, 7, 9 ,18, 90]
number_len = len(number_list)
i = 0
output = number_list[0]
while i  <=  number_len - 2 :
    i= i + 1
    if output > number_list[ i ]:
        output = output
    else:
        output = number_list[ i ]
print(output)
```
==自己跑出来没有大问题，但是在长度对应索引哪里试了很久。考虑用for循环该如何迭代==
```python
number_list = [15, 60, 100, 9 ,18, 90, 100, 5, 6]
number_len = len(number_list)
output = number_list[0]
for item in range(number_len - 1):
    if output <= number_list[item]:
        output = number_list[item]
    else:
        output = output
    print(output)
```
==这是一个错误的代码，结果会得到每次数组数量迭代出来的所有数字==

*视频范例*
``` python
numbers = [3, 6, 2, 8, 4, 10]
max_m = numbers[0]
for number in numbers:
    if number > max_model:
        max_m = number
print(max_model)
```
==对于for的循环迭代掌握度还是不够，在自己的第二个写法中出来就是没彻底理解迭代。遍历一般都用for循环==

## 2D Lists

each item in this list is gonna be another list
``` python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

print(matrix[0][1]) = 2
```

可以直接更改矩阵中数值
`matrix[0][1]= 20`

```python
for row in matrix:
    print(row)
# 前三行

for row in matrix:
    for item in row:
        print(item)
# 所有数字
```

## List methods
``` julia
numbers = [5, 2, 1, 7, 4]
numbers.append(20)
print(numbers)
# [5, 2, 1, 7, 4, 20] 20被加到最后

numbers = [5, 2, 1, 7, 4]
numbers.insert(0, 10) 
print(numbers)
# 插入到对应的index前面

numbers.remove(5)
print(numbers)


numbers.clear()
print(numbers)
# []得到一个empty list

numbers = [5, 2, 1, 7, 4]
numbers.pop()  #把列表的末尾删除，pop也有射击的意思
print(numbers)


print(numbers.index(5)) #0
print(numbers.index(5)) #erro 没有对应数据

print(50 in numbers) # False

numbers = [5, 2, 1, 5, 7, 4]
print(numbers.count(5)) #2 2个5在list中

print(numbers.sort()) 
#输出得到None 因为排序是方法，Is an object in python， which absence of a value.
# 没有返回任何值

numbers.sort()
print(numbers)
# 得到从新排序的list

numbers.sort()
numbers.reverse()
print(numbers)
# sorted in descending order

numbers2 = numbers.copy()
numbers.append(10)
print(numbers2) #对于list2 无影响
```
### exercise
remove the duplicates in a list

``` python
# for item in numbers2:
numbers = [2, 2, 4, 6, 3, 4, 6, 1]
uniques = []
for number in numbers:
    if number not in uniques:
        uniques.append(number)
print(uniques)
```
==牛逼==

# Tuples
Unlike list, cannot modify them.
Tuples are immutable.

basic method for tuples are account and index 
advanced need like `_add_`
``` python
numbers = (1, 2, 3)
print(numbers[0])
```

## Unpacking
把一组数据分成单独的不同的数据，避免多次运用list 名字
```python
coordinates = (1, 2, 3)
x, y, z = coordinates
```
not only limited in tuples, but also can used to list.
# Dictionaries
each key is associated with a value.
curly braces`{}`
each key should be unique
value can be everything
```python
customer ={
		   "name": "John Smith",
		   "age": 30,
		   "is_vertified": True
}

customer["name"]
customer["Name"] # erro, sensitive to captial

print(customer.get("name"))
print(customer.get("birthday" , "Jan 1 1980"))
#会把没有的再不报错的情况下加入数据。

customer["name"] = "Jack Smith" #更新

customer["birthday"] = "Jan 1 1980" # add a new key
"
```
### exercise
把输入的数字转换成英语
```python
number = {
    "1" : "one",
    "2" : "two",
    "3" : "three",
    "4" : "four",
    "5" : "five",
    "6" : "six",
    "7" : "seven",
    "8" : "eight",
    "9" : "nine",
    "0" : "zero"
}

shuju =input("Phone: ")
output = ""

for trans in shuju:
    output = output + number[trans]
    print(output)
```
==同样的问题，，忘记把print提前，还在循环里，会得到迭代过程，同时忘记加入空格==

范例
```python
phone = input("Phone: ")
digits_mapping = {
    "1": "One",
    "2": "Two",
    "3": "Three",
    "4": "Four"
}
output = ""
for ch in phone:
    output += digits_mapping.get(ch, "!") + " "
print(output)
```
 ==`digits_mapping.get(ch, "!")`== 后面的 ”！“ 是为了区分如果没有再dictionary里的key。且不会报错。

## Emoji converter

```python
message = input(">")
words = message.split(' ')
print(words)

```
`.split() method`
`message.split(' ')` 中的`( )` use as a boundary to separae the string into multiple words
会得到分开单词的list，且每个单词为string格式
```python
message = input(">")
words = message_users.split(' ')
emojis = {
        ":)": "😊",
        ":(": "😢"
    }
output_in_function = ""
for word in words:
    output += emojis.get(word, word) + " "
print(output)
```
# Functions
A container for a few lines of code taht perform a specific task.
```python
def function_name():
    #行为
```
colon 冒号是为了告诉python我们要定义下面一大块代码。 退出对齐退出代码块。 最好留下两行以上空行

无论何时调用代码，函数内容都会被执行
调用`function_name()`
函数要优先定义于调用

```julia
function f(x,y)
     x + y 
end

# 或者直接可定义
f(x, y) = x + y

```
==julia具有多重派发的性质，python对数据状态定义较少==

```python
def greater_user(name):
    print(f'Hi {name}!')
    print('Welcome aboard')

print("start")
great_user("John")
great_user("Mary")
print("Finish")
```
*parameters* are the holes or placeholders that we define in the function for reciving information.
*arguments* are the actual pieces of information that we supply to these functions.
## Keywords arguments
```python
def greater_user(first_name, last_name):
    print(f'Hi {first_name} {last_name}!')
    print('Welcome aboard')

print("start")
great_user("John")
print("Finish")
```
==错误代码== 会得到 missing one required positional argument
`great_user("John", "Smith" )`
the first argumnet is the value for the first parameter.
一一对应，如果使用
`great_user("Smith" , "John")`会得到相反名字

==但是对于keywords arguments，**位置**可以改变==
```python
great_user(last_name = "Smith" , first_name = "John")
```
用keywords 可以增加可读性。
keywords argument 需要用在positional argument 后面
## Return Statement
```python
def square(number):
    return number * number


print(square(3))
```
如果不设置return状态
![[mosh_return.png]]
when python interpreter executes this code, first it will call the `square()` function, so the control moves to the square function and print in terminal.
By default, all functions return the value none.
If we don't have a return statement, by default, python returns none ( an object that represents the absecnce of a value. ).

## Creating a reusable function

`input()` can come in different forms, and do not want to put it in function.
```python
def emoji_converter(message):
    words = message.split(' ')
    emojis = {
        ":)": "😊",
        ":(": "😢"
    }
    output = ""
    for word in words:
        output += emojis.get(word, word) + " "
    return output


message = input(">")
print(emoji_converter(message))
```

# Exceptions

how to handle errors in python programs
为了避免程序崩溃 
`try expect`
```python

try:
    age = int(input('Age: '))
    income = 20000
    risk = income / age
    print(age)
except ZeroDivisionError:
    print('Age cannot be 0.')
except ValueError: # type of the erro
    print("Invalid value.")

```
# Classes 类

some basic type already know
* Numbers
* Strings
* Boolean
 Some Complex type
* List
*  Dictionary
* Tuple

Can use classes to define new types to model real concepts.

Pascal naming convention 首字母大写

>Programming Naming Conventions – Camel, Snake, Kebab, and Pascal Case

 *Camel Case*：start a name with a small letter. If the name has multiple words, the later words will start with a capital letter    `firstName`  ==JavaScript==

*Snake Case*: underscore (_) to separate the words.  `first_name`  ==Python==

*Kebab case*:  use a hyphen (-) instead of an underscore (_) to separate the words. `first-name`

 *Pascal case*: all words will start with capital letters. `FirstName`

==Although Python and JavaScript require you to follow different conventions when you're naming variables and functions, both languages require you to use pascal case when naming a class.==

``` python
class Point: 
    def move(self):  
    # pycharm会自动补齐 .self, vscode 不会
        print("move")

    def draw(self):
        print("draw")

```
由此完成一类的定义（==后续代码记得空行==）
An object is an instance of a class.
a class simply defines the blueprint or the template for creating objects.
The object are the actual instances based on that blue print.

to creat the object ,type the name and call it as a function. 
`Point()` creat a new object and return it.

==self 代表的是类的实例，代表当前对象的地址，而 self.class 则指向类==

```python
point1 = Point()
point1.x = 10
point1.y = 20
print(point1.x)
print(point1.y)
point1.draw()
point1.move()

```
## Constructor 构造

At the time of creating an object,

init is a short for intialized.

``` python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def move(self):
        print("move")
    def draw(self):
        print("draw")


point = Point(10,20)
print(point.x)

# 更改x的值
point.x = 11
print(point.x)


```
the `.self` is a reference to the current object.
when create a new point object. `point = Point(10,20)`, self references that object in memory.

`def __init__(self, x, y):` refer to this method  as a constructor,  to construct or creat an object.

### exercise

``` python
class Person:
    def __init__(self,name):
        self.name = name
    
    def talk(self):
        print(f"Hi I'm {self.name}")


john = Person("John Smith")
john.talk()


bob = Person("Bob Dylan")
john.talk()
```

## Inheritance
To reusing code.
Not to define the same thing twice.

``` python
class Mammal:
    def walk(self):
        print("walk")


class Dog(Mammal):
# Will inherit all the methods defned in mammal class
    pass # 路径语句，python不理解空定义


class Cat(Mammal):
    def bark(self):
        print("annoying")


dog1 = Dog()
dog1.walk()
cat1 = Cat()
cat1.walk()
cat1.bark()

```

# Modules
 we can break our codes into multiple files.
 we refer to each file as a module.

## way 1

对于已有的一个代码。保存为converters.py
``` python
def lbs_to_kg(weight):
    return weight * 0.45


def kg_to_lbs(weight):
    return weight / 0.45

```

设置一个新文件 .py

![[mosh_1111.png]]
```python
import converters # 没有后缀

print(converters.kg_to_lbs(70))
```
## way 2

import a specific function or class from a module using`from import statement`
```python
from converters import kg_to_lbs

kg_to_lbs(70)
```


### Exercise
保存第一个文件 utils.py
``` python
def find_max(numbers):
    findMax = numbers[0]
    for number in numbers:
        if findMax < number :
            findMax = number
    return findMax
```

``` python
import utils
numbers = [10,6,3,2]
max = utils.find_max(numbers)
print(max)


from utils import find_max
numbers = [10,6,3,2]
max = find_max(numbers)
print(max)
```
*python 其实有`max（）`的自带函数*
==区别开定义后求出来的int.max和作为function的max==

# Packages
packages is a container for multiple modules.
In file system, like a a directory or folder.

右键文件夹-- New -- add a new directory // pyhon package
我们可以把相关的modules都放进这个directory.

在这个文件夹中加入`__int__.py`  will treat this directory as a package.

如果加入的packages 文件夹， 自动会有cheating file


在package中定义 shipping.py文件
``` python
def calc_shipping():
    print("calc_shipping")

```

在主程序页面

``` python
import ecommerce.shipping
ecommerce.shipping.calc_shipping()


from ecommerce.shipping import calc_shipping
calc_shipping()


from ecommerce import shipping
shipping.calc_shipping()

```
其他包可以搜 pyhon 3 module index 获得


# Random Values
```python
import random

for i in range(3):
    print(random.random(1)) 
#生成3个0-1的随机数
   print(random.randint(10， 20)) 
# 整数随机数
```

```python
import random
members = ['John', 'Mary', 'Bob']
leader = random.choice(members)
```
## exercise

``` python
import random


class Dice:
    def roll(self):
        first = random.randint(1,6)
        second = random.randint(1,6)
        return (first,second)
        #可以去掉（）， python也认为是tuple


dice = Dice()
print(dice.roll())

```

# 引用文件
`pathlib` Object-oriented filesystem paths

* Absolute path: start from the current directory.
* Relative path:

``` python
from pathlib import Path

path = Path("emails")

# 判断是否存在
print(path.exists())

# 创建
print(path.mkdir())
print(path.exists())

# 删除
print(path.rmdir())
print(path.exists())

# 遍历文件
path1 = Path()
print(path1.glob('*.py'))

for flie in path1.glob('*.py'):
    print(flie)

```
`* `means everything
