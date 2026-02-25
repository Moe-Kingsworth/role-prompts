# Coding Mentor Prompt

**Act as a mentor reviewing this code:**
```python
def greet(name): 
    return "Hello, {name}!"
message = greet("Alice")
print(message)
```
**Provide corrections and explain improvements.**

Great! Let’s go through your code carefully and review it like a mentor. Here’s your original code:

```python
def greet(name): 
    return "Hello, {name}!"
message = greet("Alice")
print(message) 
```

### **1. Identify the issue**

The code will **not produce the expected output**.

Right now, the string `"Hello, {name}!"` is a **literal string**, so Python will literally print `{name}` instead of replacing it with the value of the `name` variable.

**Current output:**

```
Hello, {name}!
```

### **2. How to fix it**

There are a few ways to format strings in Python. The most common:

#### **Option A: f-strings (Python 3.6+)**

```python
def greet(name):
    return f"Hello, {name}!"  # note the f before the string
message = greet("Alice")
print(message)
```

**Output:**

```
Hello, Alice!
```

✅ This is modern, readable, and efficient.


#### **Option B: `str.format()` method**

```python
def greet(name):
    return "Hello, {}!".format(name)
message = greet("Alice")
print(message)
```

**Output:**

```
Hello, Alice!
```

✅ Works on older Python versions too.


#### **Option C: String concatenation (less recommended)**

```python
def greet(name):
    return "Hello, " + name + "!"
message = greet("Alice")
print(message)
```

**Output:**

```
Hello, Alice!
```

⚠️ Works, but can get messy with multiple variables.


### **3. Other improvements**

1. **Add type hints** (good practice for readability):

```python
def greet(name: str) -> str:
    return f"Hello, {name}!"
```

2. **Strip whitespace** (optional, for cleaner input):

```python
def greet(name: str) -> str:
    name = name.strip()
    return f"Hello, {name}!"
```

3. **Test multiple names** to make sure the function is reusable:

```python
print(greet("Bob"))
print(greet("  Charlie  "))
```

✅ **Mentor tip:** f-strings are preferred in modern Python—they’re readable, concise, and very versatile.

If you want, I can also show a **version that handles empty or missing names** gracefully, which is a common real-world improvement.

Do you want me to do that?


#  Review

The reponse was constructive, it didn't just *fix* the bug, it showed *why* the code didn't work and included step by step guidance to the solution.

The feedback was very clear it highlited the problem clearly, provided multiple solutions and also suggested best practices and improvemnet.