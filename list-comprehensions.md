# List Comprehension Assignments and Solutions

## Assignments

1. Generate a list of squares of all numbers from 1 to 20.
2. Generate a list of even numbers from 1 to 50.
3. Generate a list of numbers from 1 to 100 that are divisible by both 3 and 5.
4. Generate a list of "Fizz" for numbers divisible by 3 and "Buzz" for numbers divisible by 5 from 1 to 30.
5. Generate a list of numbers from 1 to 30, but replace each multiple of 4 with the string "Four".
6. Generate a list of cubes of all odd numbers from 1 to 30.
7. Generate a list of all prime numbers between 1 and 50.
8. Generate a list of pairs (x, y) where x is from 1 to 5 and y is from 6 to 10.
9. Generate a list of sums of pairs (x + y) where x is from 10 to 15 and y is from 20 to 25.
10. Generate a list of products of pairs (x * y) where x is from 1 to 3 and y is from 4 to 6, but only include products greater than 10.
11. Generate a list of numbers from 1 to 100, but only include those that are either less than 20 or greater than 80.
12. Generate a list of the first 20 positive integers, but replace multiples of 5 with the string "Five".
13. Generate a list of all two-digit numbers that are palindromes.
14. Generate a list of all numbers from 1 to 50 that are perfect squares.
15. Generate a list of factorials of numbers from 1 to 10.

## Solutions

```haskell
-- Assignment 1

-- Generate a list of squares of all numbers from 1 to 20
[x*x | x <- [1..20]]

-- Generalized function to generate squares of any list
listOfSquares xs = [x*x | x <- xs]

-- Assignment 2

-- Generate a list of even numbers from 1 to 50
[x | x <- [1..50], even x]

-- Generalized function to filter even numbers from any list
listOfEvens xs = [x | x <- xs, even x]

-- Assignment 3

-- Generate a list of numbers from 1 to 100 that are divisible by both 3 and 5
[x | x <- [1..100], x `mod` 5 == 0, x `mod` 3 == 0]

-- Generalized function to filter numbers divisible by both 3 and 5 from any list
divByFiveAndThree xs = [x | x <- xs, x `mod` 5 == 0, x `mod` 3 == 0]
