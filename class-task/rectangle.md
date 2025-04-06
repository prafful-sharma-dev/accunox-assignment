
# Custom Classes in Python - Rectangle Class

## Task Description

Create a `Rectangle` class with the following requirements:
- The class requires two integers, `length` and `width`, during initialization.
- An instance of `Rectangle` should be iterable.
- When iterated, it first yields the length as `{'length': <VALUE>}` and then the width as `{'width': <VALUE>}`.

## Example Code

```python
class Rectangle:
    def __init__(self, length: int, width: int):
        self.length = length
        self.width = width

    def __iter__(self):
        # Yield a dictionary for length first, then width
        yield {'length': self.length}
        yield {'width': self.width}

# Example usage:
rect = Rectangle(10, 5)
for side in rect:
    print(side)
