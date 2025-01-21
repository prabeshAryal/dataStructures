
## **What is a Stack?**
A **stack** is a linear data structure that follows the **LIFO** (Last In, First Out) principle. This means that the last item added to the stack is the first one to be removed. You can think of a stack like a stack of plates: the last plate placed on the top is the first one to be taken off.

---

## **Basic Operations**
1. **Push**: Adds an element to the top of the stack.
2. **Pop**: Removes and returns the top element from the stack. If the stack is empty, it may raise an error or return a special value.
3. **Peek/Top**: Returns the top element without removing it.
4. **isEmpty**: Checks if the stack is empty.
5. **Size**: Returns the number of elements in the stack.

---

## **Implementation**
Stacks can be implemented using:
1. **Arrays**: Fixed size, but easy to implement.
2. **Linked Lists**: Dynamic size, but requires extra memory for pointers.

### **Example in Python (using a list as a stack):**
```python
class Stack:
    def __init__(self):
        self.items = []

    def push(self, item):
        self.items.append(item)

    def pop(self):
        if not self.is_empty():
            return self.items.pop()
        else:
            raise IndexError("Pop from an empty stack")

    def peek(self):
        if not self.is_empty():
            return self.items[-1]
        else:
            return None

    def is_empty(self):
        return len(self.items) == 0

    def size(self):
        return len(self.items)

# Example usage:
stack = Stack()
stack.push(10)
stack.push(20)
print(stack.peek())  # Output: 20
print(stack.pop())   # Output: 20
print(stack.is_empty())  # Output: False
```

---

## **Applications of Stacks**
1. **Expression Evaluation**: Used in evaluating and converting infix to postfix or prefix expressions.
2. **Backtracking**: Used in algorithms like Depth-First Search (DFS).
3. **Undo Mechanism**: Used in text editors and applications for undo operations.
4. **Function Calls**: Used in managing function calls in programming through the call stack.
5. **Balancing Parentheses**: Used to check if an expression has balanced brackets (e.g., `({[]})`).

---

## **Advantages**
1. Simple and easy to implement.
2. Efficient for managing data that needs LIFO access.

---

## **Disadvantages**
1. Limited access: You can only access the top element.
2. Memory limits: In array-based implementations, the stack size must be predefined or can grow inefficiently.

