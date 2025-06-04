# its just Dump repo why are you here? check my other repo!

Absolutely! Here's the complete 2-hour Python interview with all questions, answers, and explanations, organized clearly into sections. This version is designed for interviewers or candidates to use during preparation or assessments.


---




---

⏱️ Section 1: Python Basics (0–20 mins)


---

1. What is Python, and what are its key features?

Answer:
Python is a high-level, interpreted, general-purpose programming language known for its readability and ease of use.

Key Features:

Dynamically typed

Interpreted (no need to compile)

Cross-platform

Large standard library

Supports OOP and functional programming

Open-source and community-driven



---

2. What does it mean that Python is dynamically typed?

Answer:
Python assigns data types during runtime, not in advance.

x = 10      # int
x = "ten"   # now str


---

3. What is the difference between a list and a tuple?

Answer: | List       | Tuple       | |------------|-------------| | Mutable    | Immutable   | | Slower     | Faster      | | [1, 2]   | (1, 2)    |


---

4. What is the difference between a list and a dictionary?

Answer:

List: Ordered collection accessed via index.

Dictionary: Unordered key-value pairs accessed by keys.


lst = [10, 20]
dct = {"a": 10, "b": 20}


---

5. What is the difference between == and is in Python?

Answer:

== checks value equality.

is checks memory location (object identity).


a = [1, 2]; b = [1, 2]
a == b   # True
a is b   # False


---

6. What are Python keywords?

Answer:
Reserved words like def, class, if, None, import, which cannot be used as variable names.


---

7. What is indentation in Python?

Answer:
Python uses indentation instead of braces {} to define code blocks.

if True:
    print("Hello")  # Must be indented


---

🔢 Section 2: Data Types & Operators (20–40 mins)


---

8. Difference between / and //?

Answer:

/ = float division → 5 / 2 = 2.5

// = floor division → 5 // 2 = 2



---

9. Mutable vs Immutable types in Python

Answer:

Mutable: Can be changed (e.g., list, dict)

Immutable: Cannot be changed (e.g., int, str, tuple)



---

10. Explain slicing with example

s = "Python"
s[1:4]     # 'yth'
s[::-1]    # 'nohtyP' (reverse)


---

11. Types of operators in Python

Arithmetic: + - * / // % **

Comparison: == != > <

Logical: and, or, not

Membership: in, not in



---

🔁 Section 3: Control Flow & Functions (40–60 mins)


---

12. Using if, elif, else

x = 10
if x > 10:
    print("Big")
elif x == 10:
    print("Exact")
else:
    print("Small")


---

13. Loop types in Python

for loop: Iterates over items

while loop: Runs while condition is True


for i in range(3): print(i)


---

14. Using range()

for i in range(1, 5): print(i)


---

15. Function definition example

def greet(name):
    return f"Hello, {name}"


---

16. What are *args and **kwargs?

*args: Collects positional arguments into a tuple

**kwargs: Collects keyword arguments into a dictionary


def show(*args, **kwargs):
    print(args, kwargs)


---

17. Lambda function example

square = lambda x: x * x
print(square(4))  # 16


---

📚 Section 4: Data Structures & Algorithms (60–90 mins)


---

18. Accessing dictionary keys, values, items

d = {"a": 1, "b": 2}
d.keys()     # dict_keys(['a', 'b'])
d.values()   # dict_values([1, 2])
d.items()    # dict_items([('a', 1), ('b', 2)])


---

19. Remove duplicates from list (preserving order)

def remove_duplicates(lst):
    seen = set()
    return [x for x in lst if not (x in seen or seen.add(x))]


---

20. Reverse a string

s = "hello"
print(s[::-1])


---

21. Check if a string is a palindrome

def is_palindrome(s):
    return s == s[::-1]


---

22. Count frequency in list

from collections import Counter
print(Counter([1, 2, 2, 3]))


---

23. Find max without max()

def find_max(lst):
    m = lst[0]
    for i in lst:
        if i > m:
            m = i
    return m


---

24. Linear search in list

def search(lst, target):
    for i, val in enumerate(lst):
        if val == target:
            return i
    return -1


---

⚙️ Section 5: Intermediate Concepts (90–110 mins)


---

25. Garbage collection in Python

Answer:
Python uses:

Reference counting

Cyclic GC for unreachable circular references.


import gc
gc.collect()


---

26. Virtual environment

Answer:
An isolated environment for Python projects. Helps manage dependencies.

python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows


---

27. What is NumPy?

Answer:
A numerical library for working with arrays, matrices, and high-performance math.

import numpy as np
a = np.array([1, 2, 3])


---

28. List comprehension example

squares = [x*x for x in range(5)]  # [0, 1, 4, 9, 16]


---

29. Generator example

def gen():
    yield 1
    yield 2

g = gen()
next(g)  # 1


---

30. Shallow vs Deep copy

import copy
a = [[1], [2]]
shallow = copy.copy(a)
deep = copy.deepcopy(a)

Shallow copy copies outer structure.

Deep copy recursively copies everything.



---

31. Modules and packages

Module: .py file

Package: folder with __init__.py


import math
print(math.sqrt(16))  # 4.0


---

32. Exception handling example

try:
    5 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")


---

🧱 Section 6: OOP, File I/O, Libraries (110–120 mins)


---

33. What is OOP? Four pillars?

Encapsulation

Inheritance

Polymorphism

Abstraction



---

34. Create a class and object

class Animal:
    def __init__(self, name):
        self.name = name
    def speak(self):
        return f"{self.name} makes a sound"

a = Animal("Dog")
print(a.speak())


---

35. File reading and writing

# Writing
with open("test.txt", "w") as f:
    f.write("Hello")

# Reading
with open("test.txt", "r") as f:
    print(f.read())


---

36. Use of with statement

Answer: Ensures files are closed properly even if an error occurs.


---

🔚 Optional Bonus Questions (Use if time remains)


---

37. What is a decorator in Python?

Answer:
A function that modifies another function.

def decorator(func):
    def wrapper():
        print("Before")
        func()
        print("After")
    return wrapper

@decorator
def say_hello():
    print("Hello")


---

38. Difference: @staticmethod vs @classmethod

staticmethod: No access to class or instance

classmethod: Access to class via cls



---

39. Difference: __str__ vs __repr__

__str__: Human-readable

__repr__: Unambiguous (used in debugging)



---

40. How does Python manage memory?

Answer:

Reference counting

Garbage collection

Memory pools for small objects



---

41. How do you debug a Python script?

print() statements

logging module

pdb module (Python debugger)



---

📌 Want This as a Document?

Let me know if you'd like this in:

📄 PDF

📃 Word Doc

📝 Google Docs Template

✅ Interview Score Sheet Format


I'll generate it for easy printing or digital sharing.

