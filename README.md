# EXPERIMENT 1: INTRODUCTION TO PYTHON PROGRAMMING
**Made by**: Denise Wafa B. Españo
<div style="border-bottom: 2px solid gray; margin-bottom: 10px;"></div>

The content of this repository contains Experiment 1 for our course "Advanced Computer Programming and Algorithms". This experiment covers three Python problems involving basic operations, string methods, slicing, and sequence unpacking. 
**Intended Learning Outcomes**

At the end of this laboratory activity, the script and logic demonstrate the ability to:
 
* use basic Python functions, operators, and string operations;
* manipulate strings using indexing, slicing, and built-in string methods:
* apply sequence unpacking to manipulate the elements of a list; and
* construct simple Python functions that return a specified result.

## 1. Word Rotation Problem
<div style="border-bottom: 1px solid gray; margin-bottom: 5px;"></div>
Create a function named `rotate_word()` that accepts a non-empty string. Move the first character of the string to the end while keeping all remaining characters in their original order, preserving the capitalization of every character.

The following functions and methods were used in this problem:

String slicing `[]` and indexing were utilized in order to extract specific parts of the string, capturing the rest of the word and the first letter separately

```python
text[1:] # this captures everything from the second character onwards
text[0]  # this captures only the first character
```

In order to combine them in a new order, string concatenation `+` was used

```python
text[1:] + text[0]
```

Combining them all, the final function for this problem is:

```python
def rotate_word(text):
    return text[1:] + text[0]

print(rotate_word("python"))
print(rotate_word("logic"))
print(rotate_word("Code"))
print(rotate_word("A"))
```
## 2. Username Builder Problem
<div style="border-bottom: 1px solid gray; margin-bottom: 5px;"></div>
Create a function named `make_username()` that accepts two strings: first name and last name. The function must convert all letters to lowercase, remove all spaces from the first and last names, and join the processed names with one period (.).

The following functions and methods were used in this problem:

The `.replace()` and `.lower()` methods were used in order to remove spaces and convert all letters to lowercase for both the first and last names.

```python
first = first_name.replace(" ",""). lower()
last = last_name.replace(" ", ""). lower()
```

In order to join the processed names together into a singular username, string concatenation was used to combine them with a period `(.)` separator

```python
return first + "." + last
```

Combining all, the final function for this problem is:

```python

def make_username(first_name, last_name):
    first = first_name.replace(" ", ""). lower()
    last = last_name.replace(" ", ""). lower()
    return first + "." + last

print(make_username("Ada", "Lovelace"))
print(make_username("Alan", "Turing"))
print(make_username("Ana Maria", "De Leon"))
```
## 3. Bookend Swap Problem
<div style="border-bottom: 1px solid gray; margin-bottom: 5px;"></div>

Create a function `swap_bookends()` that accepts a list containing at least two elements. Unpack the list into three variables (`first`, `middle`, and `last`) and return a new list in which the first and last elements have exchanged positions, while the elements in the middle remain in their original order.

The following functions and methods were used in this problem:

Extended sequence unpacking was utilized in order to instantly assign the first element, the last element, and a list of everything in between to their respective variables

```python
first, *middle, last = items 
```
Combining them all, the final function for this problem is:

```python
def swap_bookends(items):
    first, *middle, last = items
    return [last] + middle + [first]

print(swap_bookends([1, 2, 3, 4, 5, 6]))
print(swap_bookends(["red", "green", "blue"]))
print(swap_bookends([8, 3]))
```
<div style="border-bottom: 1px solid gray; margin-bottom: 5px;"></div>
Thank you for reading!

To see the main Python program for Programming Assignment 1, click this (https://github.com/denisewafaespano-code/ECE2112-ProgrammingAssignment1/blob/37a9c98637178f2d66dae0cd43499bdc0add57ca/Programming%20Assignment1.ipynb) and download. Open on Jupyter Notebook, then run all cells. 

**READ ME file Version History:**

August 27, 2026 - Initial README output uploaded.





