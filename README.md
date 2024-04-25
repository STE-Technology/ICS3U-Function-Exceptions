# Function Exceptions
In Python, `try` and `except` blocks are used for error handling. Here's a summary of how to use them:

### `Try` Block
The code that you think might raise an exception is placed inside the `try` block.
```python
try:
    # Code that might raise an exception
    # ...
```

### `Except` Block
If an exception occurs in the `try` block, the control immediately passes to the `except` block. Here, you can handle the exception or take appropriate action.
```python
except ExceptionType:
    # Code to handle the exception
    # ...
```

`ExceptionType` specifies the type of exception you want to catch. You can be specific (e.g., `ValueError`, `TypeError`) or use a more general `Exception` to catch any type of exception.

### Optional `Else` Block
You can include an else block after the except block, which will only execute if no exception occurs in the try block.
```python
else:
    # Code to execute if no exception occurs
    # ...
```

### Optional `Finally` Block
This block is always executed whether an exception occurred or not. It's useful for releasing external resources (like files or network connections) regardless of whether the code in the try block succeeded or not.
```python
finally:
    # Code to execute whether there is an exception or not
    # ...
```

## Example
Here's a simple example demonstrating the usage of `try` and `except`:

```python
try:
    x = int(input("Enter a number: "))
    result = 10 / x
    print("Result:", result)
except ValueError:
    print("Please enter a valid number.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
else:
    print("No exceptions occurred.")
finally:
    print("This will always execute.")
```

In this example:

- If the user enters a non-integer value, a `ValueError` will occur, and the corresponding message will be printed.
- If the user enters `0`, a `ZeroDivisionError` will occur, and the corresponding message will be printed.
- If the user enters any other number, the result will be printed along with the message saying no exceptions occurred.
- Finally, the message in the finally block will always be printed.