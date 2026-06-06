Algorithm – Organizing Containers of Balls
Step 1: Read Input
Read the number of containers n.
Read the n × n matrix representing the number of balls of each type in each container.
Step 2: Calculate Container Capacities

For each container (row):

containerSum[i] = Sum of all balls in container i

Store these values in an array containerSum.

Step 3: Calculate Ball Type Totals

For each ball type (column):

typeSum[j] = Total number of balls of type j

Store these values in an array typeSum.

Step 4: Sort Both Arrays
Sort(containerSum)
Sort(typeSum)
Step 5: Compare Arrays
If containerSum == typeSum
    Print "Possible"
Else
    Print "Impossible"
Pseudocode
Algorithm OrganizingContainers

Input: container[n][n]

Create array containerSum[n]
Create array typeSum[n]

For i ← 0 to n-1
    containerSum[i] ← 0
    For j ← 0 to n-1
        containerSum[i] ← containerSum[i] + container[i][j]

For j ← 0 to n-1
    typeSum[j] ← 0
    For i ← 0 to n-1
        typeSum[j] ← typeSum[j] + container[i][j]

Sort(containerSum)
Sort(typeSum)

If containerSum equals typeSum
    Return "Possible"
Else
    Return "Impossible"

End Algorithm
Dry Run
Input
1 1
1 1
Row Sums
Container 1 = 2
Container 2 = 2
containerSum = [2, 2]
Column Sums
Type 1 = 2
Type 2 = 2
typeSum = [2, 2]

After sorting:

[2, 2] = [2, 2]

Output:

Possible
Complexity Analysis
Time Complexity
O(n² + n log n)
O(n²) for computing row and column sums.
O(n log n) for sorting.
Space Complexity
O(n)
