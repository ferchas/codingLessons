# CyclicRotation

A zero-indexed array A consisting of N integers is given. Rotation of the array means that each element is shifted right by one index, and the last element of the array is also moved to the first place.

For example, the rotation of array A = [3, 8, 9, 7, 6] is [6, 3, 8, 9, 7]. The goal is to rotate array A K times; that is, each element of A will be shifted to the right by K indexes

```
function solution (myArry, k) {
  while(k !=0) {
    myArry.unshift(myArry.pop());
    k--;
  }
  return myArry;
```

# OddOccurrencesInArray
A non-empty zero-indexed array A consisting of N integers is given. The array contains an odd number of elements, and each element of the array can be paired with another element that has the same value, except for one element that is left unpaired.

For example, in array A such that:
```
  A[0] = 9  A[1] = 3  A[2] = 9
  A[3] = 3  A[4] = 9  A[5] = 7
  A[6] = 9
```
the elements at indexes 0 and 2 have value 9,
the elements at indexes 1 and 3 have value 3,
the elements at indexes 4 and 6 have value 9,
the element at index 5 has value 7 and is unpaired.

```
function solution (myArry) {
  myArry.forEach( function (e, p) {
    var resultElement = myArry.filter( function (ef) {
      return ef !=e;
    });

    if(resultElement.length == (myArry.length-1)) {
      console.log("the element at index " + p + " has value " + e + " and is unpaired");
    }
  });
```
