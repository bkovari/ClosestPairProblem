# ClosestPairProblem
The repository includes a Python solution for n dimensional closest pair problem. Bruteforce method implemented.

# Exercise
Your task is to create a Java/Python program which reads a text file where each line contains the coordinates of a multidimensional point, and then looks for the closest pair of points in the file. If the program has found the closest pair of points, it should output the line numbers and the coordinates of the two closest points.

The text file contains one point per line. The coordinate values are separated by a tabulator character. The coordinate values are not necessarily integers. In case of a floating point coordinate value the decimal separator is a period. 

# Solution
## Bruteforce method
Brute force method is a simple approach and provides a solution easily implementable. Basic idea is to compare each n dimensional points with each other, and calculate the distances. Afterwards, select the minimum of the distances, and return the point pair it belongs to. This is a compute heavy method, where n(n-1)/2 comparison is needed. Using this algorithm the problem can be solved in O(n^2) time where n is the number of points. Implementation can be found under */source/solution/simple_calc.py*

## Divide and conquer method
Divide and conquer method approach in n dimension is not trivial. Implementation steps are the following: first, the input set (S) needs to be divided into two halves, thenrecursively find their minimum. Choose the smallest from the two minimums (δ). After, points of S are projected to H hyperplane, where S' represents points that are within δ to H. Using δ sparsity condition, only O(n) pairs need to be recursively examined. Calculation can be done in O(n(log n)^d−1 time where d is dimension. The algorithm can be optimized up to O(n log n).


# Repository content
1) Solution code: */source/solution*
2) Unit test code: */source/test*
3) Sample files: */venv/resources* (directory I/O based operations)

# Development details
The project was made in Python 2.7 using PyCharm Community Edition IDE. Virtualenv created. No extra package is needed, only standard library used.

