js
Javascript Assignment

Level 1: Bitwise Operations function bitwiseAND(a, b) { return a & b; }

function bitwiseOR(a, b) { return a | b; }

function bitwiseXOR(a, b) { return a ^ b; }

console.log(bitwiseAND(7, 12)); console.log(bitwiseOR(7, 12));
console.log(bitwiseXOR(7, 12));

Level 2: Redundant Operations function redundant(str) { return function() { return str; }; }

const f1 = redundant("apple"); console.log(f1());

const f2 = redundant("pear"); console.log(f2());

Level 3: Get Notes Distribution function getNotesDistribution(students) { return students .flatMap(student => student.notes) // get all notes .filter(note => note >= 1 && note <= 5) // keep valid notes .reduce((acc, note) => { acc[note] = (acc[note] || 0) + 1; return acc; }, {}); }

const result = getNotesDistribution([ { name: "Steve", notes: [5, 5, 3, -1, 6] }, { name: "John", notes: [3, 2, 5, 0, -3] } ]);

console.log(result);
Js_2
STRING FUNCTIONS; Reverse a String: function reverseString(str) { return str.split('').reverse().join(''); }

console.log(reverseString("hello")); // "olleh"

Count Characters: function countCharacters(str) { return str.length; }

console.log(countCharacters("hello"));

Capitalize Words: function capitalizeWords(sentence) { return sentence .split(' ') .map(word => word.charAt(0).toUpperCase() + word.slice(1)) .join(' '); }

console.log(capitalizeWords("hello world"));

ARRAY FUNCTIONS Find Maximum: function findMax(arr) { let max = arr[0];

for (let num of arr) {
    if (num > max) {
        max = num;
    }
}

return max;
}

Find Minimum: function findMax(arr) { let max = arr[0];

for (let num of arr) {
    if (num > max) {
        max = num;
    }
}

return max;
}

Sum of Array: function sumArray(arr) { let sum = 0;

for (let num of arr) {
    sum += num;
}

return sum;
}

Filter Array: function filterArray(arr) { return arr.filter(num => num > 10); }

console.log(filterArray([5, 12, 8, 20]));

MATHEMATICAL FUNCTIONS Factorial: function factorial(n) { let result = 1;

for (let i = 1; i <= n; i++) {
    result *= i;
}

return result;
}

console.log(factorial(5));

Prime Number Check function isPrime(num) { if (num <= 1) return false;

for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) {
        return false;
    }
}

return true;
}

console.log(isPrime(7)); console.log(isPrime(10));

Fibonacci Sequence function fibonacci(n) { let sequence = [0, 1];

for (let i = 2; i < n; i++) {
    sequence.push(sequence[i - 1] + sequence[i - 2]);
}

return sequence;
}

console.log(fibonacci(7));


