# quantum-TDA
Topological data analysis on a quantum computer
---
Using an $n \times n$ distance matrix on a point cloud (potentially normalized using PCA (*"principle component analysis"*) if the data is in high enough dimensional space) we map each pairwise distance $d_{i,j}$ to a unitary $2$-qubit controlled-U gate that encodes the distance as some *"entanglement strength"* between two qubits/qudits. The measure of enranglement strength could be von Neumann entropy between each pair of qubits, or we could compair the controlled-U gate to a CNOT gate or some other standard entangling gate via an operator norm for example. Many such entanglement strength measure can be devised and we use several here and compare the different measure for performance and accuracy. 

Once the mapping is achieved, we run a persistent homology algorithm via a modified $2$-paramemeter DB-scan (one parameter for entanglement strength, the second for energy level of qubits or local clusters of qubits with respect to the first paramemeter). 
