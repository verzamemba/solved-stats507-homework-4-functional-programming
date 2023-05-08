Download Link: https://assignmentchef.com/product/solved-stats507-homework-4-functional-programming
<br>
<h1>1         Iterators and Generators</h1>

In this exercise, you’ll get some practice working with iterators and generators. <strong>Note: </strong>in this problem, the word <em>enumerate </em>is meant in the sense of returning elements, not in the sense of the Python function enumerate. So, if I say that an iterator enumerates a sequence <em>a</em><sub>0</sub><em>,a</em><sub>1</sub><em>,a</em><sub>2</sub><em>,…</em>, I mean that these are the elements that it returns upon calls to the __next__ method, <em>not </em>that it returns pairs (<em>i,a<sub>i</sub></em>) like the enumerate function.

<ol>

 <li>Define a class Fibo of iterators that enumerate the Fibonacci numbers. For the purposes of this problem, the Fibonacci sequence begins 0<em>,</em>1<em>,</em>1<em>,</em>2<em>,</em>3<em>,…</em>, with the <em>n</em>-th Fibonacci number <em>F<sub>n </sub></em>given by the recursive formula <em>F<sub>n </sub></em>= <em>F<sub>n</sub></em><sub>−1 </sub>+ <em>F<sub>n</sub></em><sub>−2</sub>. Your solution should not make use of any function aside from addition (i.e., you should not need to use the function fibo() defined in lecture a few weeks ago). Your class should support, at a minimum, an initialization method, a __iter__ method (so that we can get an iterator) and a __next__ <strong>Note: </strong>there is an especially simple solution to this problem that can be expressed in just a few lines using tuple assignment.</li>

 <li>We can generalize the Fibonacci sequence by following the same recursive procedure<em>F<sub>n </sub></em>= <em>F<sub>n</sub></em><sub>−1</sub>+<em>F<sub>n</sub></em><sub>−2</sub>, but using a different choice of initial two values for <em>F</em><sub>0 </sub>and <em>F</em><sub>1</sub>. For example, if we take <em>F</em><sub>0 </sub>= 2 and <em>F</em><sub>1 </sub>= 1, then we obtain the Lucas numbers, which are closely related to the Fibonacci numbers (<a href="https://en.wikipedia.org/wiki/Lucas_number">https://en.wikipedia.org/wiki/ </a><a href="https://en.wikipedia.org/wiki/Lucas_number">Lucas_number</a><a href="https://en.wikipedia.org/wiki/Lucas_number">)</a>. Define a class GenFibo of iterators that enumerate <em>generalized </em>Fibonacci numbers. Your class should inherit from the Fibo class defined in the previous subproblem. The initialization method for the GenFibo class should take two <em>optional </em>arguments that specify the values of <em>F</em><sub>0 </sub>and <em>F</em><sub>1</sub>, in that order, and their values should default so that F = GenFibo() results in an enumerator equivalent to the one that would have been created if you had called F = Fibo() (i.e., GenFibo() should produce an iterator over the Fibonacci numbers).</li>

 <li>Define a generator primes that enumerates the prime numbers. Recall that a prime number is any integer <em>p &gt; </em>1 whose only divisors are <em>p </em>and 1. <strong>Note: </strong>you may use the function is_prime that we defined in class (or something similar to it), but such solutions will not receive full credit, as there is a more graceful solution that avoids declaring a separate function or method for directly checking primality. <strong>Hint: </strong>consider a pattern similar to the one seen in lecture using the any and/or all</li>

 <li>This one is good practice for coding interview questions. The <em>Ulam numbers </em>are a sequence <em>u</em><sub>1</sub><em>,u</em><sub>2</sub><em>,u</em><sub>3</sub><em>,… </em>of positive integers, defined in the following way: <em>u</em><sub>1 </sub>= 1, and <em>u</em><sub>2 </sub>= 2. For all <em>n &gt; </em>2, <em>u<sub>n </sub></em>is the smallest integer that is expressible as a sum of two <em>distinct </em>terms from earlier in the sequence in <em>exactly one way</em>. See the Examples section of the Wikipedia page for an illustration: <a href="https://en.wikipedia.org/wiki/Ulam_number">https://en.wikipedia.org/wiki/ </a><a href="https://en.wikipedia.org/wiki/Ulam_number">Ulam_number</a><a href="https://en.wikipedia.org/wiki/Ulam_number">.</a> Define a generator ulam that enumerates the Ulam numbers. <strong>Hint: </strong>it will be helpful to try and break this problem into smaller, simpler subproblems. In particular, you may find it helpful to write a function that takes a list of integers t and one additional integer u, and determines whether or not u is expressible as a sum of two distinct elements of t in exactly one way.</li>

</ol>

<h1>2         List Comprehensions and Generator Expressions</h1>

In this exercise you’ll write a few simple list comprehensions and generator expressions. Again in this problem I use the term <em>enumerate </em>to mean that a list comprehension or generator expression returns certain elements, rather than in the sense of the Python function enumerate.

<ol>

 <li>Write a list comprehension that enumerates the sequence 2<em><sup>n</sup></em>−1 for <em>n </em>= 1<em>,</em>2<em>,</em>3<em>,…,</em></li>

</ol>

For ease of grading, please assign this list comprehension to a variable called pow2minus1.

<ol start="2">

 <li>The <em>Lazy Caterer’s sequence </em>is a sequence of numbers that counts, for each <em>n </em>= 0<em>,</em>1<em>,</em>2<em>,…</em>, the largest number of pieces that can be cut from a disk with at most <em>n </em>cuts (<a href="https://en.wikipedia.org/wiki/Lazy_caterer's_sequence">https://en.wikipedia.org/wiki/Lazy_caterer’s_sequence</a><a href="https://en.wikipedia.org/wiki/Lazy_caterer's_sequence">)</a>. The <em>n</em>-th number in this sequence is given by <em>p<sub>n </sub></em>= (<em>n</em><sup>2 </sup>+ <em>n </em>+ 2)<em>/</em>2, where <em>n </em>= 0<em>,</em>1<em>,</em>2<em>,…</em>. Write a generator expression that enumerates the Lazy Caterer’s sequence. For ease of grading, please assign this generator expression to a variable called caterer. <strong>Hint: </strong>you may find it useful to define a generator that enumerates the non-negative integers.</li>

 <li>Write a generator expression that enumerates the tetrahedral numbers. The <em>n</em>-th tetrahedral number (<em>n </em>= 1<em>,</em>2<em>,…</em>) is given by, where is the binomial coefficient</li>

</ol>

<em>.</em>

For ease of grading, please assign this generator expression to a variable called tetra. <strong>Hint: </strong>you may find it useful to define a generator that enumerates the positive integers.

<h1>3         Map, Filter and Reduce</h1>

In this exercise, you’ll learn a bit about map, filter and reduce operations. We will revisit these operations in a few weeks when we discuss MapReduce and related frameworks in distributed computing. In this problem, I expect that you will use only the functions map, filter and functions from the functools and itertools modules, along with the range function (and similar list-related functions) and a sprinkling of lambda expressions.

<ol>

 <li>Write a one-line expression that computes the sum of the first 10 even square numbers (starting from 4). For ease of grading, please assign the output of this expression to a variable called sum_of_even_squares.</li>

 <li>Write a one-line expression that computes the product of the first 13 primes. Youmay use the primes generator that you defined above. For ease of grading, please assign the output of this expression to a variable called product_of_primes.</li>

 <li>Write a one-line expression that computes the sum of the squares of the first 31 primes. You may use the primes generator that you defined above. For ease of grading, please assign the output of this expression to a variable called squared_primes.</li>

 <li>Write a one-line expression that computes a list of the first twenty harmonic numbers.</li>

</ol>

Recall that the <em>n</em>-th harmonic number is given by . For ease of grading, please assign the output of this expression to a variable called harmonics.

<ol start="5">

 <li>Write a one-line expression that computes the geometric mean of the first 12 tetrahedral numbers. You may use the generator that you wrote in the previous problem. Recall that the geometric mean of a collection of <em>n </em>numbers <em>a</em><sub>1</sub><em>,a</em><sub>2</sub><em>,…,a<sub>n </sub></em>is given by (. For ease of grading, please assign the output of this expression to a variable called tetra_geom.</li>

</ol>

<h1>4         Fun with Polynomials</h1>

In this exercise you’ll get a bit of experience writing higher-order functions. You may ignore error checking in this problem.

<ol>

 <li>Write a function make_poly that takes a list of numbers (ints and/or floats) coeffs as its only argument and returns a function p. The list coeffs encodes the coefficients of a polynomial, <em>p</em>(<em>x</em>) = <em>a</em><sub>0 </sub>+ <em>a</em><sub>1</sub><em>x </em>+ <em>a</em><sub>2</sub><em>x</em><sup>2 </sup>+ ··· + <em>a<sub>n</sub>x<sup>n</sup></em>, with <em>a<sub>i </sub></em>given by coeffs[i]. The function p should take a single number (int or float) x as its argument, and return the value of the polynomial <em>p </em>evaluated at x.</li>

 <li>Write a function eval_poly that takes two lists of numbers (ints and/or floats), coeffs and args. coeffs encodes the coefficients of polynomial <em>p</em>, and your function should return the list of numbers (ints and/or floats) representing the result of evaluating the polynomial <em>p </em>on each of the elements in args, in order. You should be able to express the solution to this problem in a single line (not including the function definition header, of course). Your function should make use of make_poly from the previous part to receive full credit.</li>

</ol>