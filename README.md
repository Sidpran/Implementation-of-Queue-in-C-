# Implementation-of-Queue-in-C-


**Aim:** To study and implement Queue in C++.  

**Software Required:**  
- Mingw C/C++ compiler  
- Visual Studio Code  
- Online C++ Compiler   


## 1. – Linear Queue using Array  

### Theory of Code:-

- **Queue Concept**:  
  A queue is a linear data structure that follows the **FIFO (First-In-First-Out)** principle, where the element inserted first is removed first.  

- **Fixed Size**:  
  The queue is implemented using a static array of size 5 (`#define SIZE 5`).  

- **Initialization**:  
  Two variables `start` and `end` are initialized to `-1` to represent an empty queue.  

- **Enqueue Operation**:  
  - Checks for **overflow** (`end == SIZE - 1`).  
  - If the queue is empty (`start == -1`), it sets `start = 0`.  
  - Inserts the new element at position `++end`.  

- **Dequeue Operation**:  
  - Checks for **underflow** (`start == -1 || start > end`).  
  - Removes the element at `start` and increments `start`.  

- **Display Function**:  
  - Prints all elements from `start` to `end`.  
  - Handles the case when the queue is empty.  

- **Main Function**:  
  Demonstrates the working of queue operations: enqueue, dequeue, and display.  


### Algorithm  

1. Start  
2. Initialize `start = -1`, `end = -1`, and an array of fixed size  
3. **Enqueue Operation**:  
   - If queue is full, print overflow  
   - Otherwise, insert the element at `end + 1`  
4. **Dequeue Operation**:  
   - If queue is empty, print underflow  
   - Otherwise, remove the element from `start` and increment `start`  
5. **Display Operation**:  
   - Print all elements from `start` to `end`  
6. In `main`: Perform enqueue, dequeue, and display operations  
7. Stop  


### Conclusion  

The array-based queue implementation demonstrates the core concept of **linear queue** using a fixed-size array. By managing two pointers (`start` and `end`), it supports **insertion (enqueue)**, **deletion (dequeue)**, and **display** operations effectively.  

While this approach is simple and beginner-friendly, it has limitations such as **static size** and **no reuse of freed space** (unlike circular queues). Still, it provides a strong foundation for understanding queue behavior, overflow/underflow conditions, and prepares learners for more advanced dynamic or circular queue implementations.  
