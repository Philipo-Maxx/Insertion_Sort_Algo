# Insertion Sort Algorithm

This project demonstrates the Insertion Sort algorithm, which is a simple sorting algorithm that builds the final sorted array one item at a time. It is much less efficient on large lists than more advanced algorithms such as quicksort, heapsort, or merge sort.

## Algorithm Overview

### Algorithm: `sort_insertion`

**Variables:**

- `arr`: An array of integers to be sorted.
- `i`: An index variable for iterating through the array.
- `j`: An index variable for comparing elements.
- `key`: The element being inserted into the sorted portion of the array.

**Steps:**

1. **Read Input Array:**

   - Read the array `arr` from user input.

2. **Insertion Sort Logic:**

   - Iterate over each element of the array starting from the second element (`i = 1`).
   - For each element, store it in `key` and compare it with elements in the sorted portion of the array (to its left).
   - Move elements that are greater than `key` one position to the right.
   - Insert the `key` into its correct position.

3. **Output the Sorted Array:**
   - Print the sorted array.

## JavaScript Implementation

Here’s how you can implement the Insertion Sort algorithm in JavaScript:

```javascript
function insertionSort(arr) {
  // Read the array
  // arr is expected to be an array of integers

  // Perform insertion sort
  for (let i = 1; i < arr.length; i++) {
    let key = arr[i];
    let j = i - 1;

    // Move elements of arr[0..i-1] that are greater than key
    // to one position ahead of their current position
    while (j >= 0 && arr[j] > key) {
      arr[j + 1] = arr[j];
      j--;
    }
    arr[j + 1] = key;
  }

  // Output the sorted array
  console.log(arr);
}

// Example usage
const array = [12, 11, 13, 5, 6];
insertionSort(array);
```
