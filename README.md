## 2. NFA to DFA Conversion

Explore the conversion process from Non-deterministic Finite Automata (NFA) to DFA, a crucial step in simplifying automata and optimizing language recognition.
This C++ code implements the conversion of a given Nondeterministic Finite Automaton (NFA) to its corresponding Deterministic Finite Automaton (DFA). The program takes user input for the NFA transitions and then generates the corresponding DFA transitions based on the provided NFA.

### Explanation with Example:
  Let's take a simple NFA as an example:
  
  NFA with 3 states: A, B, C
  - Transition from A to 0: B
  - Transition from A to 1: A
  - Transition from B to 0: C
  - Transition from B to 1: B
  - Transition from C to 0: C
  - Transition from C to 1: C
  
  1. The user will input the transitions for each state of the NFA:
     - From state A through 0 transition: B
     - From state A through 1 transition: A
     - From state B through 0 transition: C
     - From state B through 1 transition: B
     - From state C through 0 transition: C
     - From state C through 1 transition: C
  
  2. The program will print the NFA table:
  ```
  NFA Table
  
  _______________________________
  State   0   1
  A       B   A
  B       C   B
  C       C   C
  ```
  
  3. The program will convert the NFA to a DFA and print the DFA table:
  ```
  DFA Table
  
  _______________________________
  State   0   1
  A       B   A
  B       C   B
  C       C   C
  BC      C   B
  ```
  
  In the DFA table, a new state "BC" is added, representing the set of states {B, C} combined through the ε (epsilon) transition. The DFA has one additional state compared to the NFA.

----
