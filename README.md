# Title: Getting Started with Unit Testing in Python

# Description
In this lab, students will learn the basics of unit testing in Python using the unittest module. They will create a simple Python program and write unit tests to ensure its correctness. By the end of this lab, students will understand the importance of testing in software development and be able to apply their knowledge to write effective unit tests.

## Example Code

### program.py

```
def square(x):
    return x * x
```

### Instructions

## Installation

- Students should start by ensuring they have Python installed on their machine.
- If they don't, they can install it from the official website.
- Students should also ensure that they have the unittest module installed. If not, they can install it using pip, which comes with Python. The command is: pip install unittest.
- Create a new Python file
- Students should create a new Python file and name it program.py.
- They should add the following code to the file:

### program.py

```
def square(x):
    return x * x
```
Explain that this code defines a function that takes a number and returns its square.


### Writing Unit Tests

- Students should create a new Python file and name it **test_program.py**.
- They should start by importing the unittest module: import unittest.
- Explain that the unittest module provides a framework for writing and running tests.
- Students should then create a new test case class that inherits from **unittest.TestCase**
```
class TestProgram(unittest.TestCase):
```
- Explain that a test case class contains test methods that verify the behavior of the code under test.
- Students should now write a test method that tests the square() function:
```
class TestProgram(unittest.TestCase):
    def test_square(self):
        result = square(2)
        self.assertEqual(result, 4)
```
- Explain that the assertEqual() method checks whether the result of the function call is equal to the expected value.

In this case, the test asserts that the square of 2 is 4.

### Running Tests

- To run the tests, students should open a command prompt and navigate to the folder where the Python files are located.
- They can then run the command python -m unittest to run all the tests in the folder.
- Explain that the unittest module discovers and runs all the test cases and test methods in the files that match the pattern test*.py.
- Students should see that the test passes, indicating that the square() function works as intended.

### Improving the Tests

- Explain that it's important to write clear and descriptive test cases and test methods.
- Students should modify the test method to use a more descriptive name and add a comment:
```
class TestProgram(unittest.TestCase):
    def test_square_with_positive_number(self):
        # Test that square of a positive number returns a positive result
        result = square(2)
        self.assertEqual(result, 4)
```
