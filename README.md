# 🐍 Python Learning Guide --- Group 2 (Functions, OOP & Project Structure)


Topics Covered: 1. Functions 2. Lambda Functions 3. Classes & Objects 4.
OOP Concepts 5. Inheritance 6. Recursion 7. Enums 8. Modules 9. if
**name** == "**main**" 10. Python Virtual Environments 11.
requirements.txt

------------------------------------------------------------------------

# 1. Functions

## What is a Function?

A **function** is a reusable block of code used to perform a specific
task.

Instead of repeating code many times, we define a function once and call
it whenever needed.

### Basic Function

``` python
def greet():
    print("Hello! Welcome to Python")
    
greet()
```

### Function with Parameters

``` python
def greet(name):
    print("Hello", name)

greet("Arulesh")
```

### Function with Return Value

``` python
def add(a, b):
    return a + b

result = add(5, 3)
print(result)
```

### Default Parameters

``` python
def greet(name="User"):
    print("Hello", name)

greet()
greet("Python")
```

### Keyword Arguments

``` python
def student(name, age):
    print(name, age)

student(age=21, name="Arulesh")
```

### \*args (Multiple Arguments)

``` python
def add_all(*numbers):
    total = 0
    for n in numbers:
        total += n
    return total

print(add_all(1,2,3,4))
```

### \*\*kwargs (Keyword Arguments)

``` python
def show_info(**data):
    for key,value in data.items():
        print(key, value)

show_info(name="Arulesh", age=21)
```

------------------------------------------------------------------------

# 2. Lambda Functions

A **lambda function** is a small anonymous function written in one line.

### Normal Function

``` python
def square(x):
    return x*x
```

### Lambda Version

``` python
square = lambda x: x*x
print(square(5))
```

### Lambda with map()

``` python
numbers = [1,2,3,4]

squares = list(map(lambda x: x*x, numbers))
print(squares)
```

### Lambda with filter()

``` python
numbers = [1,2,3,4,5]

even = list(filter(lambda x: x%2==0, numbers))
print(even)
```

------------------------------------------------------------------------

# 3. Classes and Objects

## What is a Class?

A **class** is a blueprint used to create objects.

## Creating a Class

``` python
class Student:
    def __init__(self,name,age):
        self.name = name
        self.age = age
        
    def greet(self):
        print("Hi I am", self.name)
```

## Creating Objects

``` python
s1 = Student("Arulesh",21)
s1.greet()
```

### self Keyword

`self` refers to the **current object instance**.

------------------------------------------------------------------------

# 4. Object Oriented Programming (OOP)

OOP is a programming paradigm based on **objects and classes**.

Four main principles:

1.  Encapsulation
2.  Abstraction
3.  Inheritance
4.  Polymorphism

------------------------------------------------------------------------

## Encapsulation

Encapsulation means **wrapping data and methods together**.

``` python
class Bank:
    def __init__(self,balance):
        self.__balance = balance
        
    def deposit(self,amount):
        self.__balance += amount
        
    def get_balance(self):
        return self.__balance
```

------------------------------------------------------------------------

## Abstraction

Abstraction hides internal implementation details.

Example: You use

``` python
print("Hello")
```

but do not know the internal implementation.

------------------------------------------------------------------------

## Polymorphism

Same method name but different behavior.

``` python
class Dog:
    def sound(self):
        print("Bark")

class Cat:
    def sound(self):
        print("Meow")

animals = [Dog(),Cat()]

for a in animals:
    a.sound()
```

------------------------------------------------------------------------

# 5. Inheritance

Inheritance allows one class to inherit features of another class.

``` python
class Person:
    def speak(self):
        print("I am a person")

class Student(Person):
    def study(self):
        print("I am studying")
```

Usage:

``` python
s = Student()
s.speak()
s.study()
```

------------------------------------------------------------------------

# 6. Recursion

Recursion is when a function **calls itself**.

### Factorial Example

``` python
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n-1)

print(factorial(5))
```

Important: Every recursive function must have a **base condition**.

------------------------------------------------------------------------

# 7. Enums

Enums are used to define **constant values**.

``` python
from enum import Enum

class Color(Enum):
    RED = 1
    GREEN = 2
    BLUE = 3

print(Color.RED)
```

------------------------------------------------------------------------

# 8. Modules

A **module** is a Python file containing reusable code.

### Creating Module

math_module.py

``` python
def add(a,b):
    return a+b
```

### Using Module

main.py

``` python
import math_module

print(math_module.add(5,3))
```

### Built-in Modules

``` python
import math

print(math.sqrt(16))
```

------------------------------------------------------------------------

# 9. if **name** == "**main**"

Every Python file contains a special variable called `__name__`.

If the file is executed directly:

``` python
__name__ == "__main__"
```

Example:

``` python
def greet():
    print("Hello")

if __name__ == "__main__":
    greet()
```

This prevents code from running automatically when the file is imported.

------------------------------------------------------------------------

# 10. Python Virtual Environments

Virtual environments isolate project dependencies.

### Create Environment

``` bash
python -m venv venv
```

### Activate Environment

Windows:

``` bash
venv\Scripts\activate
```

Linux / Mac:

``` bash
source venv/bin/activate
```

### Install Packages

``` bash
pip install numpy
```

------------------------------------------------------------------------

# 11. requirements.txt

This file stores project dependencies.

Example:

    numpy
    matplotlib
    requests
    flask

Install all dependencies:

``` bash
pip install -r requirements.txt
```

------------------------------------------------------------------------

# Final Summary

This README covered the following **11 Python topics**:

  No   Topic
  
  ---- ---------------------------
  
  1    Functions
  
  2    Lambda Functions
  
  3    Classes & Objects
  
  4    OOP Concepts
  
  5    Inheritance
  
  6    Recursion
  
  7    Enums
  
  8    Modules
  
  9    if **name** == "**main**"
  
  10   Virtual Environments
  
  11   requirements.txt
  

------------------------------------------------------------------------

End of Document
