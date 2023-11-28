# qu-bootcamp-deutsch-jozsa algorithm

## Introduction

The Deutsch-Jozsa algorithm is one of the earliest quantum algorithms that shows a quantum computer's advantage over classical computers. It aims to solve the "black-box" problem, where we are given a function, and we need to determine whether the function is constant or balanced.

In the classical world, to find this answer for a given function f, we would need to evaluate f(x) for half of all possible inputs to determine if the function is constant or not. However, with the Deutsch-Jozsa algorithm, we can solve this problem with just one function evaluation, making it exponentially faster than the classical approach.

## Oracle

In the Deutsch-Jozsa algorithm, the oracle represents an unknown function f: {0, 1}^n → {0, 1}. The function takes an n-bit input and produces a single bit as output. The oracle's task is to implement this function as a quantum operator.

Constant Function: If the function f(x) returns the same output for all possible inputs x, it is considered a constant function. In this case, the oracle's quantum operator performs an identity transformation on the output qubit. Mathematically, if f(x) = c for all x, where c is either 0 or 1, the oracle applies the identity transformation I on the output qubit.

Balanced Function: If the function f(x) returns different outputs for exactly half of all possible inputs x, it is considered a balanced function. In this case, the oracle's quantum operator applies a NOT gate (X gate) to the output qubit. Mathematically, if f(x) takes the value 0 for exactly half of the inputs x and 1 for the other half, the oracle applies the X gate to the output qubit.

The goal of the Deutsch-Jozsa algorithm is to efficiently determine whether the unknown oracle represents a constant or balanced function with just one function evaluation using a quantum computer.
       
![deutsch-jozsa algorithm Oracle](https://upload.wikimedia.org/wikipedia/commons/b/b5/Deutsch-Jozsa-algorithm-quantum-circuit.png)
## Task


1.The user chooses the number of qubits for the input qu-bits.

2.The algorithm randomly selects whether the oracle represents a constant or balanced function. Specifically:

  * For a constant oracle, the output register will always be in a fixed state, either all zeros or all ones, regardless of the input.   
  * For a balanced oracle, exactly half of the possible input combinations will result in the output register being all zeros, and the other half will result in the 
   output register being all ones.

3.Using Qiskit, we implement the Deutsch-Jozsa algorithm to determine the nature of the randomly generated oracle's function (constant or balanced).

## Output

1-Display the randomly generated oracle's type (constant or balanced).

2-Present the quantum circuit representing the Deutsch-Jozsa algorithm with the chosen number of qubits.

3-Display the result of the algorithm, indicating whether the oracle's function is constant or balanced.

4-Provide comments in the code to explain each step of the algorithm and the representation of the oracle in the quantum circuit.




# References

> [Qiskit documentation Quantum query algorithms ]([https://learn.qiskit.org/course/algorithms/query-algorithms](https://learning.quantum.ibm.com/course/fundamentals-of-quantum-algorithms/quantum-query-algorithms))
>    
> [introduction to classical and quantum computing-book](https://www.thomaswong.net/introduction-to-classical-and-quantum-computing-1e3p.pdf)
