# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
from abc import ABC, abstractmethod
import math

class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass

class Rectangle(Shape):
    def __init__(self, length=5, breadth=4):
        self.length = length
        self.breadth = breadth

    def calculate_area(self):
        return self.length * self.breadth

class Circle(Shape):
    def __init__(self, radius=3):
        self.radius = radius

    def calculate_area(self):
        return math.pi * self.radius * self.radius

r = Rectangle()
c = Circle()

print("Area of Rectangle =", r.calculate_area())
print("Area of Circle =", round(c.calculate_area(), 2))

## Output
<img width="1472" height="863" alt="Screenshot 2026-06-01 140308" src="https://github.com/user-attachments/assets/c78aa22e-f47e-4d69-b2c0-bda622059a8a" />

## Result
Thus, the abstract class Shape and its abstract method calculate_area() were successfully implemented in the Rectangle and Circle subclasses.
