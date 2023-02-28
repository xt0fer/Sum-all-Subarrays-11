# Subarray Sum (50 pts)

A subarray is any contiguous block of an array's elements. Given an array of integers, find the sum of all elements of all subarrays of that array.

### Example

For example, a three element array [4, 5, 6] can be made into the following subarrays:

- 1 element subarrays: [4], [5], [6]
- 2 element subarrays: [4,5], [5,6]
- 3 element subarrays: [4, 5, 6]

The sum of all subarrays is `4+5+6 + (4+5)+(5+6) + (4+5+6) = 50`.

### Function Description

subArraySum has the following parameter(s): 

- int arr[n]: an array of integers to process

#### Returns:

int: an integer representing the sum of all subarrays of the given array.

#### Constraints

`1 ≤ n ≤ 2×10^5 (20,000)`
`1 ≤ arr[i] ≤ 10^3 (1000), where 0 ≤ i < n`


```javascript
//var arr =  [ 1, 2, 3];
//var arr =  [ 1, 1, 1];
var arr = [4, 5, 6];

function subArraySum(a) {
    sum = 0;
    return sum; // this fails
}

var result = subArraySum(arr);
console.log(result);
```

### Input Format For Custom Testing

Input from stdin will be processed as follows and passed to the function:

The first line contains an integer n, the number of elements in arr. Each of the n subsequent lines contains an integer describing `arr[i] where 0 ≤ i < n`.

### Sample Case 0

#### Sample Input

```
STDIN     Function
-----     -----
3      →  arr[] size n = 3
1      →  arr = [1, 2, 4]
2
4
```

#### Sample Output

20

#### Explanation

We find the following six subarrays:

1. [1]: The sum of all the elements of this subarray is 1. 
2. [2]: The sum of all the elements of this subarray is 2. 
3. [4]: The sum of all the elements of this subarray is 4.
4. [1, 2]: The sum of all the elements of this subarray is 1 + 2 = 3.
5. [2, 4]: The sum of all the elements of this subarray is 2 + 4 = 6.
6. [1,2,4]: The sum of all the elements of this subarray is 1+2+4 = 7.

The sum of all the elements of all the subarrays is 1+2+4+3+6+7 = 23.

### Sample Case 1

#### Sample Input

```
STDIN     Function
-----     -----
3      →  arr[] size n = 3
1      →  arr = [1, 1, 1]
1
1
```
#### Sample Output

10

#### Explanation
We find the following six subarrays:

1. [1]: The sum of all the elements of this subarray is 1.
2. [1]: The sum of all the elements of this subarray is 1.
3. [1]: The sum of all the elements of this subarray is 1.
4. [1, 1]: The sum of all the elements of this subarray is 1 + 1 = 2.
5. [1, 1]: The sum of all the elements of this subarray is 1 + 1 = 2.
6. [1,1,1]: The sum of all the elements of this subarray is 1+1+1= 3.

The sum of all the elements of all the subarrays is 1+1+1+2+2+3 = 10.
