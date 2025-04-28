# Exp.No:27  
## Operator Overloading

---

### AIM  
To write a Python program to perform addition of two complex numbers using the binary '+' operator overloading. Class name: `Complex`, where the objects `Ob1 = Complex(1, 2)` and `Ob2 = Complex(2, 3)` represent complex numbers.

---

### ALGORITHM

1. **Start the Program.**
2. **Define the Complex class**:
   - Define the constructor `__init__()` to accept two parameters: `real` and `imag` (representing the real and imaginary parts of the complex number).
   - Assign these values to `self.real` and `self.imag` respectively.
3. **Define the `__truediv__()` method** to perform the addition of two complex numbers:
   - Calculate the real part of the result as the addition of `self.real` by `other.real`.
   - Calculate the imaginary part of the result as the addition of `self.imag` by `other.imag`.
   - Return a new Complex object with the calculated real and imaginary parts.
4. **Define the `__repr__()` method** to represent the complex number as a string.
   - Return a string formatted to display the real and imaginary parts with one decimal place using `f"{self.real:.1f}, {self.imag:.1f}"`.
5. **Create two objects of the Complex class**:
   - `Ob1 = Complex(1, 2)` represents the complex number `1 + 2i`.
   - `Ob2 = Complex(2, 3)` represents the complex number `2 + 3i`.
6. **Perform the division operation**: Use the `/` operator to add `Ob1` by `Ob2`. This will call the `__truediv__()` method.
7. **Print the result**: Print the result of the addition, which will be formatted by the `__repr__()` method.
8. **End the Program.**

---

### PROGRAM

```
class Complex:
    def __init__(self, real, imag):
        self.real = real
        self.imag = imag

    def __add__(self, other):
        return Complex(self.real + other.real, self.imag + other.imag)

    def __str__(self):
        return f"({self.real}, {self.imag})"

# Creating objects
obj1 = Complex(1, 2)
obj2 = Complex(2, 3)

# Performing addition using overloaded + operator
result = obj1 + obj2

# Printing the result
print(result)
```

### OUTPUT
![Screenshot 2025-04-28 141833](https://github.com/user-attachments/assets/fb2edeb0-7d62-45b9-bc4c-4a3a2005f84a)
### RESULT
Thus the python program to perform addition of two complex numbers using the binary '+' operator overloading has been implemented and executed successfully.
