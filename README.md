# LinkedListAPI in C

This project implements a **generic doubly linked list** in C, supporting any data type via function pointers for printing, comparing, and deleting data. It includes utility functions for list creation, node insertion, retrieval, and memory management.

---

## Features

- Generic `List` structure supporting any data type
- Custom function pointers for print, delete, and compare
- Insert at front or back
- Retrieve data from front or back
- Clear or free entire list

---

## Getting Started

### Files

- `LinkedListAPI.h` – Header file with list and node definitions  
- `LinkedListAPI.c` – Source file with implementation

### Example Usage

```c
List* myList = initializeList(printFunc, deleteFunc, compareFunc);

int* num = malloc(sizeof(int));
*num = 42;

insertBack(myList, num);

int* frontVal = (int*)getFromFront(myList);

freeList(myList);
```

Make sure your function pointers match the following signatures:

```c
char* printFunc(void* data);
void deleteFunc(void* data);
int compareFunc(const void* a, const void* b);
```

---

## Function Overview

| Function             | Description                            |
|----------------------|----------------------------------------|
| `initializeList()`   | Creates a new empty list               |
| `initializeNode()`   | Creates a node with user data          |
| `insertFront()`      | Adds a node at the front               |
| `insertBack()`       | Adds a node at the end                 |
| `getFromFront()`     | Gets data from the head                |
| `getFromBack()`      | Gets data from the tail                |
| `clearList()`        | Frees all nodes, keeps the list struct |
| `freeList()`         | Frees all nodes and the list struct    |

---

## Requirements

- C compiler (e.g., `gcc`)
- Custom data handlers (print/delete/compare functions)

---

## License

This project is open-source and free to use for educational or personal use.
