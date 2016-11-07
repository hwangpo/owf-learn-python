# Functions

It is good practice to break code into functions that perform specific tasks.
This ensures that code logic is easier to understand and maintain.

## Function Names

Coding conventions vary between languages, programmers, and projects.
The Style Guide for Python Code provides guidance for function names:  [https://www.python.org/dev/peps/pep-0008/#function-names](https://www.python.org/dev/peps/pep-0008/#function-names).

In summary, use lowecase names with words separated by underscores.  Or, use "camelCase" but only if already in use.
For a new project, pick a style that is appropriate given other conventions and remain consistent.

## Function Documentation

Refer to the [Documentation]("documentation") section.

## Order of Functions

To facilitate code review, functions should generally be alphabetized unless there is a reason to group/order differently.:w

## Returning Values From Functions

Python, like other languages, has conventions for how variables are passed to functions, and whether those variables can be changed.
Articles on the topic can be confusing, especially to beginning programmers,
for example:  [http://www.python-course.eu/passing_arguments.php](http://www.python-course.eu/passing_arguments.php).
To simplify, keep the following in mind:

* Mutable objects are those that can be modified.  For example, a list that is passed to the function can have items added in the function.

* Immutable objects (primitives like strings, numbers) cannot be modified and new copies are made inside the function.
Therefore, a function that needs to return such objects will need to enclose the object in a mutable object like a list in the function parameters, or
return the new immutable object(s) as the return value, a new list, tuple, etc.