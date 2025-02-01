# Reversing a Linked List

## Introduction

Reversing a linked list means reversing the order of nodes in the list. It is a common problem that can be solved using iteration or recursion. In this guide, we will demonstrate how to reverse a singly linked list using Python.

## Steps to Reverse a Linked List

### 1. Initialize Pointers

We use three pointers to reverse the list:
- `prev` — Initially set to `None` (as the new tail will point to `None`).
- `current` — Points to the head of the list.
- `next_node` — Temporarily stores the next node to avoid losing reference.

### 2. Traverse the List

We loop through the list and change the next pointer of each node to point to its previous node.

### 3. Update the Head

After the loop completes, set the head of the list to the new first node.

## Python Code Example

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None
    
    def append(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        last_node = self.head
        while last_node.next:
            last_node = last_node.next
        last_node.next = new_node
    
    def print_list(self):
        current = self.head
        while current:
            print(current.data, end=" -> ")
            current = 

