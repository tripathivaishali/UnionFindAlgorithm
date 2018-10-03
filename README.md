# UnionFindAlgorithm
Under this project, a Union-Find Class has been developed that takes integer value N from command line to determine the number of “sites.” It then generates random pairs of integers between 0 to N-1, calling connected() to determine if they are connected and union() if not. Loop until all sites are connected then print the number of connections generated. The hypothesis to be proved here is that the number of pairs generated to complete the graph (i.e. to reduce the number of components from n to 1) is ~ 1/2 n ln n where ln n is the natural logarithm of n.
I.	Overview
Under this assignment, a Union-Find Class has been developed that takes integer value N from command line to determine the number of “sites.” It then generates random pairs of integers between 0 to N-1, calling connected() to determine if they are connected and union() if not. Loop until all sites are connected then print the number of connections generated.
The hypothesis to be proved here is that the number of pairs generated to complete the graph (i.e. to reduce the number of components from n to 1) is ~ 1/2 n ln n where ln n is the natural logarithm of n.

II.	Abbreviations Used
N: Number of sites entered by the user

III.	Conclusion
Using the union-find method, we tried to execute the algorithm to connect all the sites provided by user. We generated random pairs of numbers and connecting them till a single component is achieved (or the graph is completely connected). It has been observed that the number of random pairs generated in order to complete the grid of N sites is approximately equal to 
(N/2)ln(N)
IV.	Approach
There are 2 interfaces and 1 class that contains main() method:
1.	Interface Connections
Methods:
	boolean isConnected(int p, int q);	//p and q are the random sites generated
	connect(int p, int q);			//to connect p&q if isConnected returns false
2.	Interface US that extends Connections
Methods:
	int components();			//returns number of components/ connected sets
	int find(int p);				//finds the index of a site
	union(int p, int q);			//this unions the randomly generated pair of sites
	default boolean isConnected(int p, int q)	//returns the connection status
3.	UnionFindClass
Implements all these methods.

