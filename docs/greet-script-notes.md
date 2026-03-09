# Greet Script Notes

## 1. What does this script do?

The `greet.py` script is a simple command-line program that takes a person's name as input and prints a personalized greeting. It accepts the name as a command-line argument and outputs "Hello, [name]!" to the console.

For example:
- Input: `python greet.py Alice`
- Output: `Hello, Alice!`

## 2. How do you run it?

To run the script, use the following command:

```bash
python script/greet.py <name>
```

Replace `<name>` with the actual name you want to greet.

**Example:**
```bash
python script/greet.py Bob
```

This will output:
```
Hello, Bob!
```

**Error handling:**
If you run the script without providing a name, it will display:
```
Usage: python greet.py <name>
```

## 3. What Python concepts are used in the code?

### a. **Module Import**
```python
import sys
```
Imports the `sys` module, which provides access to system-specific parameters and functions, including command-line arguments.

### b. **Function Definition**
```python
def greet(name):
    print(f"Hello, {name}!")
```
Defines a reusable function that takes a `name` parameter and prints a greeting.

### c. **F-String (Formatted String Literal)**
```python
f"Hello, {name}!"
```
A Python 3.6+ feature that allows embedding expressions inside strings using curly braces `{}`.

### d. **Command-Line Arguments**
```python
sys.argv
```
A list containing the script name and command-line arguments. `sys.argv[0]` is the script name, and `sys.argv[1]` is the first argument (the name).

### e. **Conditional Statement**
```python
if len(sys.argv) < 2:
```
Checks if fewer than 2 arguments were provided (script name + name argument). If true, displays an error message.

### f. **Main Guard (if __name__ == "__main__")**
```python
if __name__ == "__main__":
```
A Python idiom that ensures the code only runs when the script is executed directly, not when imported as a module in another script.

### g. **Error Handling with sys.exit()**
```python
sys.exit(1)
```
Exits the program with a non-zero status code (1) to indicate an error occurred.
