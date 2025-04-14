# JavaScript-Basic

// JavaScript Assignment Solutions.
//1. Create a variable to store your name and display it in an alert.
 let name = "Raehanah"; 
alert("My name is" + name) //This can only work in a browser.

// 2. Declare two number variables and show their sum, difference, product, and quotient.
let x = 10, y = 5; 
console.log("Sum:", x + y);
console.log("Difference:", x - y); 
console.log("Product:", x * y); 
console.log("Quotient:", x / y); 

// 3. Write a program that converts Celsius to Fahrenheit.
function celsiusToFahrenheit(celsius) {
  return (9/5) * celsius + 32;
}
console.log("100 Celsius in Fahrenheit:", celsiusToFahrenheit(100));

// 4. Create a program that calculates the area of a rectangle using variables for length and width.
function calculateRectangleArea(length, width) {
  return length * width;
}
console.log("Area of rectangle with length 5 and width 10:", calculateRectangleArea(5, 10) );

// 5. Write code that checks if a number is even or odd and displays the result.
function checkEvenOdd(number) {
  return number % 2 === 0 ? "Even" : "Odd";
}
console.log("Is 7 even or odd?", checkEvenOdd(7));


// 6. Create a program that determines if a year entered is a leap year.
function isLeapYear(year) {
  if (year % 4 === 0) {
    if (year % 100 === 0) {
      return year % 400 === 0;
    } else {
      return true;
    }
  }
  return false;
}
console.log("Is 1900 a leap year?", isLeapYear(1900));

// 7. Write a function that returns the reverse of a string input.
function reverseString(str) {
  return str.split('').reverse().join('');
}
console.log(reverseString("bird"))
// 8. Create a function that counts the number of vowels in a string.
function countVowels(str) {
  let count = 0;
  const vowels = 'aeiouAEIOU';
  for (let i = 0; i < str.length; i++) {
    if (vowels.includes(str[i])) {
      count++;
    }
  }
  return count;
}
console.log(countVowels("beautiful"))
// 9. Write a program that finds the largest number in an array of 5 numbers.
function largest(arr) { 
    return Math.max(...arr); 
}
console.log(largest([4, 9, 1, 7, 3])); 

// 10. Create a function that checks if a string is a palindrome.
function isPalindrome(str) { 
let reversed = str.split('').reverse().join(''); return str === reversed; 
} 
console.log(isPalindrome("madam"));

// 11. Write code that calculates the factorial of a number.
function factorial(n) { 
    if (n === 0) return 1;
    return n * factorial(n - 1); 
} 
console.log(factorial(5)); 

// 12. Create a function that generates a random number between two given values.
function randomNumberBetween(min, max) { 
    return Math.floor(Math.random() * (max - min + 1)) + min; 
} 
console.log(randomNumberBetween(1, 10)); 

// 13. Write a program that converts a number of seconds into hours, minutes, and seconds.
function convertSeconds(totalSeconds) {
  const hours = Math.floor(totalSeconds / 3600);
  const remainingSeconds = totalSeconds % 3600;
  const minutes = Math.floor(remainingSeconds / 60);
  const seconds = remainingSeconds % 60;
  return `${hours} hours, ${minutes} minutes, ${seconds} seconds`;
}
console.log(convertSeconds(4000))
// 14. Create a program that checks if a number is prime.
function isPrime(number) {
  if (number <= 1) return false;
  for (let i = 2; i <= Math.sqrt(number); i++)
  {
    if (number % i === 0) return false;
  }
  return true;
}
console.log(isPrime(17))
// 15. Write a function that capitalizes the first letter of each word in a sentence.
function capitalizeWords(sentence) {
  return sentence.split(' ').map(word => word.charAt(0).toUpperCase() + word.slice(1)).join(' ');
}
console.log(capitalizeWords("i love chocolate"));
// 16. Create a program that calculates the sum of all numbers from 1 to n.
function sumToN(n) {
  return (n * (n + 1)) / 2;
}
console.log(sumToN(15));
// 17. Write code that finds the average of numbers in an array.
function averageOfArray(arr) {
  const sum = arr.reduce((a, b) => a + b, 0);
  return sum / arr.length;
}
console.log(averageOfArray([2, 5, 1, 6, 7]));
// 18. Create a function that removes duplicate values from an array.
function removeDuplicates(arr) {
  return [...new Set(arr)];
}
console.log(removeDuplicates([4, 3, 8, 4, 6, 17, 3, 2, 2, 11, 5, 7, 6, 8]));
// 19. Write a program that counts down from 10 to 1, then displays "Blast off!".
function countDown(){
    for (let i = 10; i >= 1; i--) {
    console.log(i);
  }
  console.log("Blast off!");
}
countDown()

// 20. Create a function that determines if a string contains only numbers.
function containsOnlyNumbers(str) {
  return /^\d+$/.test(str);
}
console.log(containsOnlyNumbers("12345"))

// 21. Write code that finds the second smallest number in an array.
function secondSmallest(arr) {
  const sortedArr = [...arr].sort((a, b) => a - b);
  return sortedArr[1];
}
console.log(secondSmallest([3, 5, 2, 7, 4]))

// 22. Create a program that displays the multiplication table for a given number.
function multiplicationTable(number) {
  for (let i = 1; i <= 12; i++) {
    console.log(`${number} x ${i} = ${number * i}`);
  }
}
multiplicationTable(5)

// 23. Write a function that validates if a password meets specific criteria (at least 8 characters, one uppercase, one lowercase, one number).
function validatePassword(password) {
  const hasLength = password.length >= 8;
  const hasUpper = /[A-Z]/.test(password);
  const hasLower = /[a-z]/.test(password);
  const hasNumber = /[0-9]/.test(password);
  return hasLength && hasUpper && hasLower && hasNumber;
}
console.log(validatePassword("p@ssword1"))

// 24. Create code that simulates a simple calculator with basic operations.
  function calculator(a, b, operator) {
  switch (operator) {
    case '+':
      return a + b;
    case '-':
      return a - b;
    case '*':
      return a * b;
    case '/':
      return b !== 0 ? a / b : "Cannot divide by zero";
    default:
      return "Invalid operator";
  }
}

console.log(calculator(10, 5, '+')); 
console.log(calculator(10, 5, '-')); 
console.log(calculator(10, 5, '*')); 
console.log(calculator(10, 5, '/')); 
console.log(calculator(10, 0, '/')); 
// 25. Write a program that finds all factors of a given number.
function findFactors(num) {
  const factors = [];
  for (let i = 1; i <= num; i++) {
    if (num % i === 0) {
      factors.push(i);
    }
  }
  return factors;
}
console.log(findFactors(12)); 
// 26. Create a function that checks if two strings are anagrams.
function areAnagrams(str1, str2) {
  const cleanStr = s => s.toLowerCase().replace(/[^a-z]/g, '').split('').sort().join('');
  return cleanStr(str1) === cleanStr(str2);
}
console.log(areAnagrams("listen", "silent")); 
// 27. Write a program that generates the Fibonacci sequence up to n terms.
function fibonacci(n) {
  const sequence = [];
  for (let i = 0; i < n; i++) {
    if (i < 2) {
      sequence.push(i);
    } else {
      sequence.push(sequence[i - 1] + sequence[i - 2]);
    }
  }
  return sequence;
}
console.log(fibonacci(10)); 
// 28. Create code that sorts an array of numbers without using the built-in sort method.
function bubbleSort(arr) {
  const sorted = [...arr];
  for (let i = 0; i < sorted.length; i++) {
    for (let j = 0; j < sorted.length - i - 1; j++) {
      if (sorted[j] > sorted[j + 1]) {
        [sorted[j], sorted[j + 1]] = [sorted[j + 1], sorted[j]];
      }
    }
  }
  return sorted;
}
console.log(bubbleSort([5, 3, 8, 1, 2])); 
// 29. Write a function that counts how many times a specific element appears in an array.
function countOccurrences(arr, element) {
  return arr.filter(item => item === element).length;
}
console.log(countOccurrences([1, 2, 3, 2, 2, 4], 2)); 
// 30. Create a shopping cart program where users can add items, remove items, and calculate the total price.
class ShoppingCart {
  constructor() {
    this.items = [];
  }

  addItem(name, price) {
    this.items.push({ name, price });
  }

  removeItem(name) {
    this.items = this.items.filter(item => item.name !== name);
  }

  calculateTotal() {
    return this.items.reduce((total, item) => total + item.price, 0);
  }

  viewCart() {
    return this.items;
  }
}

const cart = new ShoppingCart();
cart.addItem("Book", 15);
cart.addItem("Pen", 5);
cart.addItem("Notebook", 10);
cart.removeItem("Pen");
console.log(cart.viewCart()); 
console.log("Total:", cart.calculateTotal()); 