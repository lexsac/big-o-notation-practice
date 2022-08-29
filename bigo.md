Step One: Simplifying Expressions
Simplify the following big O expressions as much as possible:
1) O(n)
2) O(n)
3) O(1) (constant)
4) (INCORRECT, should be O(n^3))
5) O(n)
6) O(log n) (INCORRECT, should be O(n))
7) O(n log n)
8) O(2^n)
9) O(1) (constant)
10) O(n + n^2 + nlog(n)) (INCORRECT, should be O(n^2))

Step 2: Calculating Time Complexity

function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
Time Complexity: O(n)


function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
Time Complexity: O(n)


function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}
Time Complexity: O(1) (constant)


function onlyElementsAtEvenIndex(array) {
  let newArray = [];
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray.push(array[i]);
    }
  }
  return newArray;
}
Time Complexity: O(n)


function subtotals(array) {
  let subtotalArray = [];
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray.push(subtotal);
  }
  return subtotalArray;
}
Time Complexity: O(n^2) 


function vowelCount(str) {
  let vowelCount = {};
  const vowels = "aeiouAEIOU";

  for (let char of str) {
    if(vowels.includes(char)) {
      if(char in vowelCount) {
        vowelCount[char] += 1;
      } else {
        vowelCount[char] = 1;
      }
    }
  }

  return vowelCount;
}
Time Complexity: O(2n) (INCORRECT, should be O(n))



Part 3 - short answer
Answer the following questions

True or false: n^2 + n is O(n^2). True
True or false: n^2 * n is O(n^3). True
True or false: n^2 + n is O(n). False
What’s the time complexity of the .indexOf array method? O(n)
What’s the time complexity of the .includes array method? O(n)
What’s the time complexity of the .forEach array method? O(n) (INCORRECT, O(n) at least but depends on implmentation)
What’s the time complexity of the .sort array method? Depends on implementation (INCORRECT, O(n log n)
What’s the time complexity of the .unshift array method? O(1) (INCORRECT, O(n))
What’s the time complexity of the .push array method? O(1)
What’s the time complexity of the .splice array method? O(n)
What’s the time complexity of the .pop array method? O(1)
What’s the time complexity of the Object.keys() function? O(n)

BONUS

What’s the space complexity of the Object.keys() function? O(n)