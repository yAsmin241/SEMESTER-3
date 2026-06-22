# SECJ2013 Data Structure and Algorithm - Portfolio Self-Reflections

---

## 📊 Assignment 1: Comparative Analysis of Quadratic Sorting Algorithms

* **Focus Areas**: Bubble Sort, Improved (Optimized) Bubble Sort, Selection Sort, Insertion Sort, Big-O Efficiency, Comparison/Swap performance benchmarks.
* **Reflective Insight**: 
  * Implementing and manually tracking execution traces for these foundational quadratic algorithms highlighted how minor algorithmic refactorings significantly change compute constraints. 
  * Specifically, integrating a boolean flag (`sorted`) in the **Improved Bubble Sort** dropped our required comparisons for an array from 10 down to 4. This reinforced how early-termination mechanisms safeguard processor cycles.
  * Analyzing **Selection Sort** mathematically demonstrated that it maintains the lowest swap overhead (only 2 swaps compared to 6 in the other approaches). This taught me that when memory operations or hardware data-writes are resource-expensive, minimizing data movement via Selection Sort is more optimal than minimizing comparison checks.

---

## 📑 Assignment 2: Real-World Application of Stacks (Undo/Redo Text Editor)

* **Focus Areas**: Linear Data Structures, Last-In-First-Out (LIFO) Topology, Array-Based vs. Pointer-Based Stacks, Dynamic Memory Allocation, Edge-Case Handling.
* **Reflective Insight**: 
  * This assignment successfully connected abstract Abstract Data Types (ADTs) with practical system architectures by mocking up a fully functional text editor undo/redo buffer. Leveraging the LIFO principle allowed our software engine to seamlessly reverse or re-apply sequential typing states.
  * Comparing **Array-Based vs. Pointer-Based Linkage** revealed deep trade-offs in software optimization:
    * Array structures provided O(1) random-access simplicity but suffered from fixed sizing constraints ($top == 100 - 1$) and high memory waste.
    * Pointer systems (Linked Lists) eliminated arbitrary indexing ceilings, allocating blocks on-demand. However, they introduced structural complexity like proper pointer dereferencing and meticulous garbage management to prevent damaging system memory leaks.

---

## 🔄 Lab Exercise 2: Mastery of Recursion Concepts

* **Focus Areas**: Divide and Conquer Foundations, Base Cases vs. General Cases, Call Stack Traversal, Stack Overflows.
* **Reflective Insight**: 
  * Debugging recursive calculations like `powerOfTwo` and `sumUpTo` highlighted the absolute criticality of defining robust base cases. I observed firsthand how omitting or mistyping a termination flag causes the runtime engine to trigger infinite loops, blowing past memory safety and causing fatal stack overflows.
  * Refactoring these algorithms taught me to think cleanly about complex problems by breaking them down into self-similar mathematical steps ($n + sumUpTo(n-1)$). It also emphasized writing pure code structures without taking shortcut dependencies on built-in math libraries like `<cmath>`'s `pow()`.

---

## ✈️ Mini Project: Flight Passenger Queue Simulation System

* **Focus Areas**: Object-Oriented Simulation, First-In-First-Out (FIFO) Architecture, Use Case Specifications, UML Modelling, Priority Enqueuing, Collaborative Lifecycle Management.
* **Reflective Insight**: 
  * Our final deliverable converted messy, stressful real-world airport terminal check-in queues into an organized, fair digital simulation executing on a strict FIFO pattern. 
  * As a core developer, I was specifically responsible for drafting the core **System Design (UML & System Diagrams)** and writing the source logic for the **`Passenger Class`**. Programmatically modeling customer properties (Regular, Business, VIP tiers) alongside active memory address pointers (`Passenger *next`) taught me how to create clean, modular data contracts. 

### 🛠️ Key Technical Implementations
* **FIFO Fairness**: Implemented reliable enqueue and dequeue loops protecting multi-tiered airline processing from queue-jumping bottlenecks.
* **Object Isolation**: Kept class scopes decoupled, linking the Passenger structures cleanly into our higher-level `Queue` and `Simulation` systems.
* **Team Synergy**: Working tightly with my group mates (Brendan, Jiale, and Salman) via targeted code integrations and review sessions taught me how to collectively navigate memory allocation issues and validate input bugs under tight timeline goals.

