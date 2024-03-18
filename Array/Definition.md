# Array Definitions

An array is a data structure consisting of a collection of elements, each identified by an index or key. Arrays are used to store multiple values in a single variable, as opposed to declaring separate variables for each value.

## Static Arrays

Static arrays have a fixed size, determined at compile time. The size and structure of the array cannot be changed once it is created.

## Dynamic Arrays

Dynamic arrays can change in size during program execution. They allow for more flexible memory usage and can expand or contract as needed. When a dynamic array exceeds its current capacity and requires resizing, it typically doubles its size to accommodate additional elements. This resizing operation is a linear-time operation O(n), but when considered over a long sequence of operations, the time cost is "amortized" to O(1) per operation. This is because the doubling strategy means that resize operations become less frequent as the array grows.

# Array Operations and Their Big-O Time Complexity

| Operation                      | Big-O Time | Amortized Time |
| ------------------------------ | ---------- | -------------- |
| r/w i-th element               | O(1)       | O(1)           |
| Insert/Remove End              | O(1)       | O(1)           |
| Insert Middle                  | O(n)       |                |
| Remove Middle                  | O(n)       |                |
| Double Size When Full (Resize) | O(n)       | O(1)           |

The Big-O notation describes the worst-case scenario with regard to time complexity, providing an upper bound on the time required for a given operation. For dynamic arrays, operations like reading or writing the i-th element and inserting or removing at the end generally have a time complexity of O(1), indicating that they can be performed in constant time. The amortized time for doubling the size of the array is also O(1), which takes into account the total cost of resize operations over a sequence of insertions. Operations that involve inserting or removing elements in the middle of the array have a time complexity of O(n), where n is the number of elements in the array, because these operations require shifting the remaining elements to maintain the array's contiguous nature.
