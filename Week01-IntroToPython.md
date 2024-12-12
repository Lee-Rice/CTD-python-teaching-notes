| Week | Topic | Learning Objectives | Key Resources |
|-------|-------|--------------------|-------------|
| 1 | Intro to Python|Students will learn the basics of Python programming, including variables, data types, operators, control flow statements, and functions. They will also practice debugging their code.  | TBD |

# Overview

Here is an overview of what students cover this week:

* 1.1 [Python Basics](https://github.com/Code-the-Dream-School/python-essentials/blob/main/lessons/01IntroToPython.md#11-python-basics)
  * Python Variables
    * Python variables don't need to be declared before assignment.
    * Variable data types can change be changed dynamically.
  * Python data types
    * Integer (int): Whole numbers (e.g., 42, -3)
    * Float (float): Decimal numbers (e.g., 3.14, -0.5)
    * String (str): Text (e.g., "hello", "world")
    * Boolean (bool): Represents True or False values
  * Type Casting
    * Type casting occurs using conversion functions like `int()`, `float()`, and `str()`.
  * [Operators in Python](https://github.com/Code-the-Dream-School/python-essentials/blob/main/lessons/01IntroToPython.md#operators-in-python)
    * Python has a variety of means to perform operations on variables and values.

* 1.2 [Flow Control](https://github.com/Code-the-Dream-School/python-essentials/blob/main/lessons/01IntroToPython.md#12-control-flow)
  * [Conditional Statements](https://github.com/Code-the-Dream-School/python-essentials/blob/main/lessons/01IntroToPython.md#conditional-statements)
    * Execute code when certain conditions are met.
    * Can be nested in each other.
  * Loops
    * Allow code to be repeated multiple times.
    * Types
      * `for` loop
      * `while` loop
    * Loop control statements
      * `break`
      * `continue`

* 1.3 [Functions](https://github.com/Code-the-Dream-School/python-essentials/blob/main/lessons/01IntroToPython.md#13-functions)
  * Defining/calling a python function using mulitple parameters and a return.
    * Basic example:

        ``` python
        def greet(greeting, name):
            return greeting + " " + name

        print(greet("Hello,", "Bob!"))
        ```

* 1.4 [Error Handling](https://github.com/Code-the-Dream-School/python-essentials/blob/main/lessons/01IntroToPython.md#14-error-handling)
  * Managed with `try`, `except`, `else`, and `finally` blocks.
    * Handing errors with `try`, `except`, `else`:

      ``` python
      try:
          result = 10 / 2
      except ZeroDivisionError:
          print("Error: Division by zero is not allowed.")
      else:
          print(f"Success! The result is {result}.")
      ```

    * Using `finally`:

      ``` python
      try:
        file = open("example.txt", "r")
        content = file.read()
      except FileNotFoundError:
        print("Error: File not found.")
      finally:
        file.close()
        print("File closed.")
        ```

    * Raising exceptions with `raise`

      ``` python
      def check_age(age):
        if age < 18:
          raise ValueError("Age must be 18 or older.")
          return True
        try:
          check_age(16)
        except ValueError as e:
          print(e)
        ```

* 1.5 [Basic Debugging](https://github.com/Code-the-Dream-School/python-essentials/blob/main/lessons/01IntroToPython.md#15-basic-debugging)
  * Debugging with Print Statements
    * Example:

      ``` python
      def multiply(a, b):
        result = a * b
        print("Result is:", result)  # Print to check the result
        return result
        multiply(3, 5)  # Output: Result is: 15
        ```

  * Debugging with Logging
    * Example:

     ``` python
     # Step 1
     import logging

     # Step 2
     logging.basicConfig(level=logging.DEBUG)
     
     # Step 3
     def multiply(a, b):
      logging.debug(f"Multiplying {a} and {b}")
      result = a * b
      logging.info(f"Result is: {result}")
      return result
    multiply(3, 5)
    ```

# Guidance for Mentors

Potential FAQs or trouble spots from this week include:

* Resources
  * [Official Python3 documentation](https://docs.python.org/3/index.html).
  * [Official Python FAQs](https://docs.python.org/3/index.html)
  * [Official Python Tutorial](https://docs.python.org/3/tutorial/index.html)
  * [Python HOWTO](https://docs.python.org/3/howto/index.html1)
* Type hinting
  * Depending on other programming languages a student is familiar with, they may be wondering if variable/parameter types need to be defined in a function.
    * While Python supports type hinting, it is not natively enforced.
    * Reference: [Support for Typehints](https://docs.python.org/3/library/typing.html#typing-support-for-type-hints)
* Why do I sometimes get strange results when doing basic math operations?
  * Python decimals are not exact.
  * Reference: [Why are floating-point calculations so inaccurate?](https://docs.python.org/3/faq/design.html#why-are-floating-point-calculations-so-inaccurate)
* Why doesn't Python use brackets and instead use indentation?
  * The language designer believes that indenation makes code more easily readable.
    * Reference: [Why does Python use indentation for grouping of statements?](https://docs.python.org/3/faq/design.html#why-does-python-use-indentation-for-grouping-of-statements)
* Where can I find additional information on how to use Python logging?
  * The Python documentation has a good [Logging HOWTO](https://docs.python.org/3/howto/logging.html)

# Assignment Rubric

You can mark the student's assignment as complete if their submission:

* [ ] Uses proper syntax and good Python logic to answer the questions.
* [ ] Complete each task as defined by the assignment.
* [ ] Runs properly without errors (unless generating an error is part of the task).
* [ ] Uses Python style `for` loops; as opposed to JavaScript style `for` loops.

## Example solutions

Note: Solutions will vary based on student style and input values used.

### Task 1

``` python
# Task 1.1

num_str = "559"
num_int = int(num_str)
age = 27

print("Task 1.1: ")
print(num_int + age)
print("\n")

# Task 1.2
height = 4.2
height_str = str(height)
units = "meters"
full_str = height_str + " " + units
print("Task 1.2: ")
print(full_str)
print("\n")

# Task 1.3
age_float = float(age)
print("Task 1.3: ")
print(age_float)
print("\n")
```

### Task 2

``` python
# Task 2.1
num_1 = int(input("Please a number: "))
num_2 = int(input("Please enter a second non-zero number: "))

# Task 2.2
add_nums = num_1 + num_2
sub_nums = num_1 - num_2
mult_nums = num_1 * num_2
try:
    div_nums = num_1 / num_2
except:
    print("ZeroDivisionError: Please enter a non-zero number for the second entry.\n")

# Task 2.3
print("num_1 + num_2 = " + str(add_nums))
print("num_1 - num_2 = " + str(sub_nums))
print("num_1 * num_2 = " + str(mult_nums))
if num_2 != 0:
    print("num_1 / num_2 = " + str(div_nums))
else:
    print("Unable to divide num_1 by zero.")
```

### Task 3

``` python
# Task 3.1
user_score = float(input("Please enter your score as a float value: "))

# Task 3.2
letter_grade = "A"

if user_score >= 80 and user_score <= 89:
    letter_grade = "B"
elif user_score >= 70 and user_score <= 79:
    letter_grade = "C"
elif user_score >= 60 and user_score <= 69:
    letter_grade = "D"
elif user_score < 60:
    letter_grade = "F"

# Task 3.3
print("Your grade is: " + letter_grade)
```

### Task 4

``` python
# Task 4.1
def calculate_average(nums):
    '''Calculates and returns the average of a list of numbers.'''

# Task 4.2
    num_sum = 0
    list_length = 0
    for num in nums:
        num_sum += num
        list_length += 1
    return num_sum // list_length

# Task 4.3
list_of_ints = [1, 2, 3, 4, 5]
print("The average is: " + str(calculate_average(list_of_ints)) + "\n")`
```

### Task 5

``` python
# Task 5.1
def divide_numbers(num_1, num_2):
    '''Returns the result of dividing two numbers.'''

# Task 5.2
    try:
        return num_1 / num_2
    except ZeroDivisionError:
        return "ZeroDivisionError: Please enter a non-zero number for the second entry.\n"

user_num_1 = int(input("Please enter a number: "))
user_num_2 = int(input("Please enter a second non-zero number: "))

# Task 5.3
print("\nThe result of " + str(user_num_1) + " / " + str(user_num_2) + " is: ")
print(divide_numbers(user_num_1, user_num_2))
```
