Practice Problems
=================
This is a collection of practice/interview questions I've heard and my solutions.

Almost Twins
------------
Given a binary search tree and a value `x`, find the node with value immediately
greater than `x`. For example, given the following binary tree and value `x = 9`,
your algorithm would return the root node with value `x = 10`.

          10
        /    \
       7     15
     /  \   /  \
    4    9 11  20
        /
       8

Decimal to Binary
-----------------
Given an Integer, return the binary representation of that Integer as a String.
For example:

    0.to_b  => '0'
    2.to_b  => '10'
    6.to_b  => '110'
    28.to_b => '11100'

Fibonacci
---------
Given N, print the first N Fibonacci numbers. For example, `fib_sequence(6)` should
return:

    0 1 1 2 3 5

Luhn Algorithm
--------------
The Luhn algorithm, also known as the "mod 10" algorithm, is a simple checksum
formula used to validate a variety of identification numbers. Given a numeric
input, the algorithm works as follows:

1. Counting from the check digit, which is the rightmost, and moving left,
   double the value of every second digit.

2. Sum the digits of the products (e.g., `10 = 1 + 0 = 1, 14 = 1 + 4 = 5`)
   together with the undoubled digits from the original number.

3. If the total modulo 10 is equal to 0 (if the total ends in zero) then the
   number is valid according to the Luhn formula; else it is not valid.

Here are some example inputs:

    luhn?('42')   => true    # 2 + 8 = 10
    luhn?('9001') => true    # 1 + 0 + 0 + (1 + 8) = 10
    luhn?('43')   => false   # 3 + 8 = 11
    luhn?('0175') => false   # 5 + (1 + 4) + 1 + 0 = 11

Minimum Match
-------------
Given an input text and a set of characters, return the shortest substring of the
input text which contains those characters. For example, given the input text
`abbcabbbc` and the characters `abc`, return the string:

    abbc

More Than Perms
---------------
Given a set of letters and a length N, produce all possible output. (Not permutation).
For example, give the letter `(p,o)` and length of `3`, produce the following
output(in any order you want, not just my example order):

    ppp ppo poo pop opp opo oop ooo

Another example would be given `(a,b)` and length `2`:

    ab aa bb ba

Palindrome
----------
A palindrome is a word or phrase that can be read the same forwards and backwards. Some
examples of palindromes include:

    race car
    dad
    A man, a plan, a canal, Panama

Write a method that returns `true` when a String is a palindrome, `false` otherwise.
Remember to ignore white space, punctuation, and letter case.

Pivot
-----
Given an array of unsorted integers, find the pivot point `n` in the array where
the sum of `input(0..n)` = sum of `input(n+1..input.size)`. Values in the input
array may be positive or negative.

For example, given the input:

    [1, 2, 3, 0, 4, 2]

The pivot point would be `3`, the index of element with the value `0` because:

    input[0] + input[1] + input[2] = input[4] + input [5]
       1     +    2     +    3     =    4     +    2

Primes
------
Write a function that accepts an integer `n` and returns a list of all prime
numbers between 1 and `n`. For example, given the input `n = 10`, the function
would return:

    [1, 2, 3, 5, 7]

Reorder Priority
----------------
Given any input text and a 'preference string', organize the characters in the
input text to match the priority of the characters in the preference string.
For example, given the input text `banana` and the preference string `can`,
return the string `aaannb`. Given the input text `house` and the preference
string `soup`, two possible solutions would be `soueh` or `souhe`.

Reverse Polish Notation
-----------------------
Reverse Polish Notation (RPN) is a mathematical notation wherein every operator
follows all of its operands. Write a a function `rpn` that accepts an array of
operands and operators and returns the result. Here are some examples:

    rpn(['2', '3', '+'])            => 5
    rpn(['5', '1', '-'])            => 4
    rpn(['2', '3', '+', '5', '*'])  => 25
    rpn(['2', '3', '5', '+', '*'])  => 16

Secret Santa
------------
Given an array of names, generate a hash that can be used for the 'secret santa'
game. For example, given the array:

    ['thom', 'sally', 'doug', 'steve']

Some valid solutions may include:

    { "thom"  => "sally", "sally" => "steve", "steve" => "doug", "doug" => "thom"  }
    { "steve" => "sally", "sally" => "thom" , "thom"  => "doug", "doug" => "steve" }

Similar Set
-----------
Given two arrays, return a new array containing those elements which the two
arrays have in common. For example, given the arrays:

    [1, 2, 'a', 'b']
    [2, 3, 'b', 'c']

The returned array would be:

    [2, 'b']

Spiral Matrix
-------------
Print a 2D int matrix in sprial order. For example, given the array:

    [[1 ,2, 3],
     [4 ,5, 6],
     [7 ,8, 9]]

Return the solution:

    [1, 2, 3, 6, 9, 8, 7, 4, 5]

Sum Of Evil
-----------
Given a number, come up with all of the possible ways to insert `+` and `-` in
that number. For example, given `123`, possible output would be:

    1+23
    1+2+3
    1-23
    1-2+3
    1-2-3
    1+2-3
    12+3
    12-3
