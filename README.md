# Library Management System

## Overview
This project is a simple Library Management System developed in Python as part of a practical assignment for a Systems Analysis and Development course. The system allows users to:

- Add new books
- List all books
- Search books by title
- Visualize the number of books per genre using Matplotlib

## Features
- **Book Management**: Classes and functions to handle book creation, listing, and searching.
- **Visualization**: Generates a chart showing the number of books per genre.
- **Interactive Program Loop**: A custom `ProgramLoop` class enables running the program in a continuous interactive loop, allowing users to navigate menus, execute actions, return to previous menus, or exit the program.

## ProgramLoop Class

`ProgramLoop` is a utility class that manages the interactive menu, handling user input, looping the program, and executing commands safely. It supports reserved commands:

* `[0]`: Stop the program
* `[-1]`: Go back to the previous menu

```python
# Example

program = ProgramLoop([
    ((1, "Add new book"), lambda: register_book()),
    ((2, "List books"), lambda: list_books()),
    ((3, "Search book by title"), lambda: search_book_by_title()),
    ((4, "Dashboard"), lambda: show_books_dashboard()),
])

program.run()
```
