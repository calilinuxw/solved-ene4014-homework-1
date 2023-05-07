Download Link: https://assignmentchef.com/product/solved-ene4014-homework-1
<br>
<strong>Exercise 1 </strong>Write a function

gcd : int → int → int

that returns the greatest common divisor (GCD) of two given non-negative integers. Use the Euclidean algorithm based on the following principle (for two integers <em>n </em>an <em>m </em>such that <em>n </em>≥ <em>m</em>):

<em>2</em>

<strong>Exercise 2 </strong>Write a function

merge : int list → int list → int list

that takes two integer lists sorted in descending order and returns a new sorted integer list that includes every element in the two given lists. For example,

merge [3;2;1] [5;4] = [5;4;3;2;1]

merge [5;3] [5;2] = [5;5;3;2] merge [4;2] [] = [4;2] merge [] [2;1] = [2;1]

<em>2</em>

<strong>Exercise 3 </strong>Write a function

range : int → int → int list

range lower upper generates a sorted list of integers in the range [lower … upper]. If lower is greater than upper, the function returns the empty list. For example,

<table width="202">

 <tbody>

  <tr>

   <td width="92">range13</td>

   <td width="24">=</td>

   <td width="87">[1;2;3]</td>

  </tr>

  <tr>

   <td width="92">range (−2) 2</td>

   <td width="24">=</td>

   <td width="87">[−2;−1;0;1;2]</td>

  </tr>

  <tr>

   <td width="92">range22</td>

   <td width="24">=</td>

   <td width="87">[2]</td>

  </tr>

  <tr>

   <td width="92">range2 (−2)</td>

   <td width="24">=</td>

   <td width="87">[]</td>

  </tr>

 </tbody>

</table>

<em>2</em>

type formula = TRUE | FALSE

| NOT of formula

| ANDALSO of formula * formula

| ORELSE of formula * formula

| IMPLY of formula * formula

| LESS of expr * expr and expr = NUM of int

| PLUS of expr * expr

| MINUS of expr * expr

<strong>Exercise 4 </strong>Considering the above definition of propositional formula, write a function eval : formula → bool

that computes the truth value of a given formula. For example, eval (IMPLY (IMPLY (TRUE, FALSE), TRUE))

evaluates to <em>true</em>, and

eval (LESS (NUM 5, PLUS (NUM 1, NUM 2)))

evaluates to <em>false</em>. <em>2</em>

<strong>Exercise 5 </strong>Binary trees can be inductively defined as follows:

type btree = Empty | Node of int * btree * btree

For example, the following t1 and t2 are binary trees.

let t1 = Node (1, Empty, Empty) let t2 = Node (1, Node (2, Empty, Empty), Node (3, Empty, Empty)) let t3 = Node (1, Node (2, Node (3, Empty, Empty), Empty), Empty)

Write a function height : btree → int

that computes the height of a given binary tree. The height of a given binary tree is inductively defined as follows:

heightEmpty = 0

(heightl) + 1            (heightl <em>&gt; </em>heightr)

height (Node n<em>,</em>l r

(heightr) + 1      (otherwise)

For example,

<table width="292">

 <tbody>

  <tr>

   <td width="258">heightEmpty</td>

   <td width="27">=</td>

   <td width="7">0</td>

  </tr>

  <tr>

   <td width="258">heightt1</td>

   <td width="27">=</td>

   <td width="7">1</td>

  </tr>

  <tr>

   <td width="258">heightt2</td>

   <td width="27">=</td>

   <td width="7">2</td>

  </tr>

  <tr>

   <td width="258">heightt3<em>2</em><strong>Exercise 6 </strong>Write a function</td>

   <td width="27">=</td>

   <td width="7">3</td>

  </tr>

 </tbody>

</table>

balanced : btree → bool<em>.</em>

that determines if a given binary tree is <em>balanced</em>. A tree is balanced if the tree is empty or the following conditions are met.

<ul>

 <li>The left and right subtrees’ heights differ by at most one, and</li>

 <li>The left subtree is balanced, and</li>

 <li>The right subtree is balanced.</li>

</ul>

For example,

<table width="167">

 <tbody>

  <tr>

   <td width="108">balancedEmpty</td>

   <td width="24">=</td>

   <td width="35">true</td>

  </tr>

  <tr>

   <td width="108">balancedt1</td>

   <td width="24">=</td>

   <td width="35">true</td>

  </tr>

  <tr>

   <td width="108">balancedt2</td>

   <td width="24">=</td>

   <td width="35">true</td>

  </tr>

  <tr>

   <td width="108">balancedt3</td>

   <td width="24">=</td>

   <td width="35">false</td>

  </tr>

 </tbody>

</table>

where t1, t2, and t3 are defined in Exercise 5. <em>2</em>

<strong>Exercise 7 </strong>The fold function for lists

fold : (‘a → ‘b → ‘a) → ‘a → ‘blist → ‘a

recombines the results of recursively processing its constituent parts, building up a return value through use of a given combining operation. For example,

foldfa [b1;<em>…</em>;bn] = f (<em>…</em>(f (fab1) b2)<em>…</em>) bn<em>.</em>

Extend the following function that takes three lists. Write a function

fold3 : (‘a → ‘b → ‘c → ‘d → ‘a) → ‘a → ‘blist → ‘clist → ‘dlist → ‘a

of which meaning is defined as follow:

fold3fa [b1;<em>…</em>;bn] [c1;<em>…</em>;cn] [d1;<em>…</em>;dn]

= f (<em>…</em>(f (fab1c1d1) b2c2d2)<em>…</em>) bncndn<em>.</em>

You may assume that all the given lists are of the same length. <em>2</em>

<strong>Exercise 8 </strong>Write a function

(iter

The function returns the identity function (fun x → x) when <em>n </em>= 0. For example,

(iter <em>n </em>(fun x -&gt; x + 2)) 0

returns 2 × <em>n</em>. <em>2</em>

<strong>Exercise 9 </strong>Write a function

sigma : int * int * (int -&gt; int) -&gt; int<em>.</em>

such that sigma(a,b,f) returns Σ

<strong>Exercise 10 </strong>Write a function cartesian: ’a list -&gt; ’b list -&gt; (’a * ’b) list

that returns a list of from two lists. That is, for lists <em>A </em>and <em>B</em>, the Cartesian product <em>A </em>× <em>B </em>is the list of all ordered pairs (<em>a,b</em>) where <em>a </em>∈ <em>A </em>and <em>b </em>∈ <em>B</em>. For example, if <em>A </em>= [“<em>a</em><sup>00</sup>;“<em>b</em><sup>00</sup>;“<em>c</em><sup>00</sup>] and <em>B </em>= [1;2;3], <em>A </em>× <em>B </em>is defined to be

<em>2</em>