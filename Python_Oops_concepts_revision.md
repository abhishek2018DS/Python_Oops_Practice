## Python OOPs Concepts Revision

### Python Object-Oriented Programming (OOP) Interview Preparation

#### 1. **Class and Object:**
- **Definition:** 
    - A class is a blueprint for creating objects. It defines attributes (data) and methods (functions) that the objects will have.
    - An object is an instance of a class.
- **Example:**
    - Class: `Car`
    - Object: `my_car = Car()`
  
#### 2. **Attributes and Methods:**
- **Attributes:**
    - Characteristics or properties of an object.
- **Methods:**
    - Functions associated with a class.
- **Example:**
    ```python
    class Dog:
        def __init__(self, name, age):
            self.name = name
            self.age = age
            
        def bark(self):
            return "Woof!"
            
    my_dog = Dog("Buddy", 5)
    print(my_dog.name)  # Output: Buddy
    print(my_dog.bark())  # Output: Woof!
    ```
  
#### 3. **Constructor and Destructor:**
- **Constructor (`__init__`):**
    - Special method invoked when an object is instantiated.
    - Used for initializing object attributes.
- **Destructor (`__del__`):**
    - Special method invoked when an object is about to be destroyed.
    - Used for cleanup activities.
- **Example:**
    ```python
    class MyClass:
        def __init__(self):
            print("Constructor called.")
        
        def __del__(self):
            print("Destructor called.")
    
    obj = MyClass()  # Output: Constructor called.
    del obj  # Output: Destructor called.
    ```

#### 4. **Inheritance:**
- **Definition:**
    - The mechanism of creating a new class from an existing class.
    - Allows a class to inherit attributes and methods from another class.
- **Example:**
    ```python
    class Animal:
        def sound(self):
            return "Sound"
    
    class Dog(Animal):
        def sound(self):
            return "Woof!"
    
    my_dog = Dog()
    print(my_dog.sound())  # Output: Woof!
    ```
  
#### 5. **Polymorphism:**
- **Definition:**
    - The ability of objects to take on multiple forms.
    - Allows methods to behave differently based on the object calling them.
- **Example:**
    ```python
    class Animal:
        def sound(self):
            return "Sound"
    
    class Dog(Animal):
        def sound(self):
            return "Woof!"
    
    class Cat(Animal):
        def sound(self):
            return "Meow!"
    
    def make_sound(animal):
        return animal.sound()
    
    my_dog = Dog()
    my_cat = Cat()
    print(make_sound(my_dog))  # Output: Woof!
    print(make_sound(my_cat))  # Output: Meow!
    ```

#### 6. **Encapsulation:**
- **Definition:**
    - Bundling of data (attributes) and methods that operate on the data within a single unit (class).
    - Data hiding mechanism to restrict access to certain attributes or methods.
- **Example:**
    ```python
    class BankAccount:
        def __init__(self):
            self.balance = 0
        
        def deposit(self, amount):
            self.balance += amount
        
        def withdraw(self, amount):
            if self.balance >= amount:
                self.balance -= amount
            else:
                print("Insufficient funds.")
    
    account = BankAccount()
    account.deposit(1000)
    account.withdraw(500)
    print(account.balance)  # Output: 500
    ```
  
#### 7. **Abstraction:**
- **Definition:**
    - Process of hiding the complex implementation details and showing only the necessary features of an object.
- **Example:**
    ```python
    from abc import ABC, abstractmethod
    
    class Animal(ABC):
        @abstractmethod
        def sound(self):
            pass
    
    class Dog(Animal):
        def sound(self):
            return "Woof!"
    
    my_dog = Dog()
    print(my_dog.sound())  # Output: Woof!
    ```

#### 8. **Getter and Setter Methods:**
- **Definition:**
    - Getter methods are used to access the value of a private attribute.
    - Setter methods are used to modify the value of a private attribute.
- **Example:**
    ```python
    class Person:
        def __init__(self, name):
            self.__name = name
        
        def get_name(self):
            return self.__name
        
        def set_name(self, name):
            self.__name = name
    
    person = Person("Alice")
    print(person.get_name())  # Output: Alice
    person.set_name("Bob")
    print(person.get_name())  # Output: Bob
    ```

#### 9. **Class and Instance Variables:**
- **Class Variables:**
    - Shared among all instances of a class.
    - Defined within the class but outside any methods.
- **Instance Variables:**
    - Unique to each instance of a class.
    - Defined inside the constructor using `self`.
- **Example:**
    ```python
    class Circle:
        pi = 3.14  # Class variable
        
        def __init__(self, radius):
            self.radius = radius  # Instance variable
    
    circle1 = Circle(5)
    circle2 = Circle(10)
    print(circle1.radius)  # Output: 5
    print(circle2.radius)  # Output: 10
    print(Circle.pi)  # Output: 3.14
    ```

#### 10. **Method Overriding:**
- **Definition:**
    - Providing a new implementation for a method in the subclass, which is already present in the parent class.
- **Example:**
    ```python
    class Animal:
        def sound(self):
            return "Sound"
    
    class Dog(Animal):
        def sound(self):
            return "Woof!"
    
    my_dog = Dog()
    print(my_dog.sound())  # Output: Woof!
    ```

---


```python

```
