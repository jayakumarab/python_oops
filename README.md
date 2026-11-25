# python_oops
Object orient programming Language
# **Python OOP Concepts (Object-Oriented Programming)**

Python OOP means **Object-Oriented Programming**. It is a programming approach where we organize code using **Classes and Objects**.

OOP has 4 main concepts:

1. Encapsulation
2. Inheritance
3. Polymorphism
4. Abstraction

Let's learn each concept with simple English, Tamil explanations, and Python examples.

## **1. Class and Object (Basic)**

Before learning the four OOP concepts, understand Class and Object.

**Class:** A blueprint or template for creating objects.

**Object:** An instance of a class.

Example:

```
class Student:    name = "Jay"    age = 22    def display(self):        print(self.name)        print(self.age)# Creating an objects1 = Student()s1.display()
```

Output:

```
Jay
22
```

**Tamil:**

- Class = ஒரு மாதிரி வடிவமைப்பு (Blueprint).
- Object = அந்த Class-ஐ பயன்படுத்தி உருவாக்கப்படும் ஒன்று.

## **2. Encapsulation**

**Definition:** Encapsulation means wrapping data and methods together inside a class and controlling access to data.

Example:

```
class BankAccount:    def __init__(self, balance):        self.__balance = balance    def get_balance(self):        return self.__balance    def deposit(self, amount):        self.__balance += amountaccount = BankAccount(5000)account.deposit(2000)print(account.get_balance())
```

Output:

```
7000
```

**Tamil explanation:**

Encapsulation என்பது data-வை class-க்குள் பாதுகாப்பாக வைத்திருப்பது.

- `__balance` → Private attribute (name mangling).
- `get_balance()` → Balance பார்க்க.
- `deposit()` → பணம் சேர்க்க.

## **3. Inheritance**

**Definition:** Inheritance allows one class to acquire properties and methods from another class.

Example:

```
class Animal:    def eat(self):        print("Animal is eating")class Dog(Animal):    def bark(self):        print("Dog is barking")dog = Dog()dog.eat()dog.bark()
```

Output:

```
Animal is eating
Dog is barking
```

**Tamil explanation:**

Inheritance என்பது ஒரு Parent Class-ல் உள்ள properties மற்றும் methods-ஐ Child Class பயன்படுத்துவது.

- `Animal` → Parent Class
- `Dog` → Child Class

## **4. Polymorphism**

**Definition:** Polymorphism means one method name can have different behaviors.

Example:

```
class Dog:    def sound(self):        print("Dog barks")class Cat:    def sound(self):        print("Cat meows")dog = Dog()cat = Cat()dog.sound()cat.sound()
```

Output:

```
Dog barks
Cat meows
```

**Tamil explanation:**

Polymorphism என்றால் ஒரே method name, வெவ்வேறு செயல்பாடுகளைச் செய்வது.

Here, `sound()` behaves differently for Dog and Cat.

## **5. Abstraction**

**Definition:** Abstraction means hiding implementation details and showing only essential functionality.

Example:

```
from abc import ABC, abstractmethodclass Vehicle(ABC):    @abstractmethod    def start(self):        passclass Car(Vehicle):    def start(self):        print("Car started")car = Car()car.start()
```

Output:

```
Car started
```

**Tamil explanation:**

Abstraction என்பது உள்ளே எப்படி வேலை செய்கிறது என்பதை மறைத்து, தேவையான functionality மட்டும் வெளியே காட்டுவது.

Here:

- `Vehicle` → Abstract Class.
- `start()` → Abstract Method.
- `Car` → Implements the method.

## **Quick Revision – Four OOP Concepts**

| Concept       | Simple Meaning       | Example       |
| ------------- | -------------------- | ------------- |
| Encapsulation | Protect data         | Bank Account  |
| Inheritance   | Reuse code           | Animal → Dog  |
| Polymorphism  | Different behaviours | Dog/Cat sound |
| Abstraction   | Hide implementation  | Vehicle → Car |

## **Practice Questions**

Let's check your understanding! Try answering without looking at the explanations.

**Python OOP Quiz**

4/4 answered

**1. Which OOP concept is used to protect data inside a class?**

Inheritance

Encapsulation

Polymorphism

Abstraction

Correct!Encapsulation controls access to data inside a class.

**2. Which concept allows a child class to use parent class methods?**

Abstraction

Polymorphism

Inheritance

Encapsulation

Correct!Inheritance allows code reuse from a parent class.

**3. One method name with different behaviours is called?**

Polymorphism

Encapsulation

Inheritance

Class

Correct!Polymorphism means many forms or different behaviours.

**4. Which concept hides implementation details?**

Inheritance

Object

Abstraction

Encapsulation

Correct!Abstraction exposes essential functionality and hides implementation details.

Check Answers

# **Score: 4/4**

Try Again

**My recommendation:** Learn Python OOP in this order:

1. Class and Object
2. Constructor (`__init__`)
3. `self` keyword
4. Instance and Class variables
5. Four OOP concepts
6. Real-time OOP project using Python and FastAPI



Part 1. Class and Object
1. What is a Class?
A class is a blueprint for creating objects.

Real-life example:

Think about a student.

A student has:
- Name
- Age
- Department
- Marks
We can create a Student class to represent these details.










Python code:
class Student:    name = "Jay"    age = 22    department = "ECE"



Here:
- class → keyword to create a class.
- Student → class name.
- name, age, department → class attributes.
2. What is an Object?
An object is an instance of a class.

Example:
class Student:    name = "Jay"    age = 22s1 = Student()print(s1.name)print(s1.age)



Output:
Jay
22


Explanation:
Code	Meaning
class Student	Create a class
s1 = Student()	Create an object
s1.name	Access name
s1.age	Access age

Tamil explanation:

Class என்பது ஒரு blueprint. Object என்பது அந்த blueprint-ஐ பயன்படுத்தி உருவாக்கப்படும் instance.

For example:
- Student = Class
- Jay = Object
- Arun = Another Object
3. Multiple Objects
One class can create multiple objects.
class Student:    passs1 = Student()s2 = Student()s3 = Student()print(s1)print(s2)print(s3)



Here, all three objects belong to the same Student class.

Part 2. Constructor (__init__)
1. What is a Constructor?
A constructor is a special method that runs automatically when an object is created.

In Python, we use:
__init__()



Example:
class Student:    def __init__(self):        print("Student object created")s1 = Student()s2 = Student()



Output:
Student object created
Student object created


Notice: We didn't manually call __init__(). Python calls it when creating each object.
2. Constructor with Parameters
Now let's pass student details.
class Student:    def __init__(self, name, age):        self.name = name        self.age = ages1 = Student("Jay", 22)s2 = Student("Arun", 21)print(s1.name)print(s1.age)print(s2.name)print(s2.age)



Output:
Jay
22
Arun
21


Understand this:
- name, age → parameters.
- self.name, self.age → attributes stored in the object.
- Student("Jay", 22) → creates a Student object with those values.
Tamil: Constructor என்பது object உருவாகும்போது தானாக இயங்கும் special method.

Part 3. self Keyword
This is one of the most important Python OOP concepts.
What is self?
self refers to the current object.

Example:
class Student:    def __init__(self, name):        self.name = name    def display(self):        print("Student Name:", self.name)s1 = Student("Jay")s2 = Student("Arun")s1.display()s2.display()



Output:
Student Name: Jay
Student Name: Arun


How does self work?
Object 1
s1

self.name = "Jay"

Object 2
s2

self.name = "Arun"

Each object has its own data. self refers to whichever object is currently calling the method.

Important:
s1.display()



Python internally treats this approximately as:
Student.display(s1)



That's why self refers to s1.

Remember: self is not a Python keyword. It is a naming convention.

Part 4. Instance Variables and Class Variables
This is an important interview topic.
1. Instance Variables
Instance variables belong to individual objects.
class Student:    def __init__(self, name, age):        self.name = name        self.age = ages1 = Student("Jay", 22)s2 = Student("Arun", 21)print(s1.name)print(s2.name)



Output:
Jay
Arun


Each object has its own name and age.
2. Class Variables
Class variables are shared by all objects of a class unless an object overrides the attribute.
class Student:    college = "GRT Institute"    def __init__(self, name):        self.name = names1 = Student("Jay")s2 = Student("Arun")print(s1.college)print(s2.college)



Output:
GRT Institute
GRT Institute


Difference
Instance Variable	Class Variable
Belongs to an object	Belongs to class
Uses self	Defined directly in class
Each object can have different values	Shared by objects
Example: name, age	Example: college


Part 5. Four Main OOP Concepts
Now let's understand the four concepts with practical examples.
1. Encapsulation – Protecting Data
class BankAccount:    def __init__(self, balance):        self.__balance = balance    def deposit(self, amount):        self.__balance += amount    def get_balance(self):        return self.__balanceaccount = BankAccount(5000)account.deposit(1000)print(account.get_balance())



Output: 6000

Tamil: Data-வை class-க்குள் வைத்து, methods மூலம் access செய்வது.
2. Inheritance – Code Reusability
class Employee:    def work(self):        print("Employee is working")class Developer(Employee):    def coding(self):        print("Developer is coding")d1 = Developer()d1.work()d1.coding()



Output:
Employee is working
Developer is coding


Tamil: Parent class-ல் உள்ள functionality-ஐ Child class பயன்படுத்துவது.
3. Polymorphism – Different Behaviours
class EmailNotification:    def send(self):        print("Sending Email")class SMSNotification:    def send(self):        print("Sending SMS")e = EmailNotification()s = SMSNotification()e.send()s.send()



Output:
Sending Email
Sending SMS


Tamil: ஒரே method name வெவ்வேறு செயல்பாடுகளைச் செய்யும்.
4. Abstraction – Hiding Implementation
from abc import ABC, abstractmethodclass Payment(ABC):    @abstractmethod    def pay(self):        passclass UPI(Payment):    def pay(self):        print("UPI payment processing")p = UPI()p.pay()



Output:
UPI payment processing


Tamil: Internal implementation-ஐ மறைத்து, தேவையான functionality மட்டும் காட்டுவது.

Part 6. Real-Time Project – Student Management System
Now let's connect all these concepts.

Practical project
 Python + FastAPI


Project: Student Management API

Features:
1. Add student
2. View all students
3. View student by ID
4. Update student
5. Delete student
Architecture:
Frontend – React.js
Student management UI
FastAPI – API Routes
GET, POST, PUT, DELETE
Python OOP – Service Layer
Classes, Objects, Methods
PostgreSQL Database
Student records

Step 1 – Create Student Class
Create student.py.
class Student:    def __init__(self, student_id, name, age, department):        self.student_id = student_id        self.name = name        self.age = age        self.department = department    def display(self):        return {            "student_id": self.student_id,            "name": self.name,            "age": self.age,            "department": self.department        }



Step 2 – Create Student Management Class
Create student_service.py.
from student import Studentclass StudentService:    def __init__(self):        self.students = []    def add_student(self, student):        self.students.append(student)        return "Student added successfully"    def get_students(self):        return [            student.display()            for student in self.students        ]



Step 3 – Connect with FastAPI
Create main.py.
from fastapi import FastAPIfrom student import Studentfrom student_service import StudentServiceapp = FastAPI()service = StudentService()@app.post("/students")def add_student(    student_id: int,    name: str,    age: int,    department: str):    student = Student(        student_id,        name,        age,        department    )    return service.add_student(student)@app.get("/students")def get_students():    return service.get_students()



Run:
pip install fastapi uvicorn
uvicorn main:app --reload


Open:

http://127.0.0.1:8000/docs

You can test the API using Swagger UI.