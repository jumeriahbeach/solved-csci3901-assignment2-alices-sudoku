Download Link: https://assignmentchef.com/product/solved-csci3901-assignment2-alices-sudoku
<br>
Get practice in writing test cases.

Problem

<strong>Write test cases </strong>for Alice’s Sudoku class.

A Sudoku puzzle is a square grid of <em>n</em>×<em>n </em>sub-grids, each of which is itself a grid of <em>n</em>×<em>n </em>cells, where <em>n </em>is a positive integer. In total, there are <em>n</em><sup>2</sup>×<em>n</em><sup>2 </sup>individual cells. An example is shown in fig. 1. The goal of the puzzle is to enter the numbers 1 to <em>n</em><sup>2 </sup>into the cells of the grid such that:

<ul>

 <li>Every row contains all numbers from 1 to <em>n</em><sup>2</sup></li>

 <li>Every column contains all numbers from 1 to <em>n</em><sup>2</sup></li>

 <li>Every sub-grid contains all numbers from 1 to <em>n</em><sup>2</sup></li>

</ul>

A slight generalization of Sudoku is to use a collection of <em>n</em><sup>2 </sup>distinct items instead of the numbers for 1 to <em>n</em><sup>2</sup>. For instance, in a 9 × 9 Sudoku, we can use the letters a to i to fill the cells instead of numbers. In the version of Sudoku we consider in this assignment, any set of <em>n</em><sup>2 </sup>unique characters will be allowed.

The Sudoku class Alice is tasked with writing has the following methods:

public Sudoku<strong>(int size)                </strong>A constructor for a Sudoku grid with size<sup>2</sup>×size<sup>2 </sup>cells.

public boolean setPossibleValues(String values) Takes a string of length size<sup>2 </sup>where the characters of values are the unique items allowed in the cells. Returns false if any error occurred and true otherwise.

public boolean setCellValue(int x, int y, char letter) Sets the value in cell (x, y) to the character letter. public boolean solve() Solve the puzzle, returning true if a solution was found and false otherwise.

<table width="397">

 <tbody>

  <tr>

   <td width="19">5</td>

   <td width="19">3</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">7</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td rowspan="9" width="57"> </td>

   <td width="19">5</td>

   <td width="19">3</td>

   <td width="19"><em>4</em></td>

   <td width="19"><em>6</em></td>

   <td width="19">7</td>

   <td width="19"><em>8</em></td>

   <td width="19"><em>9</em></td>

   <td width="19"><em>1</em></td>

   <td width="19"><em>2</em></td>

  </tr>

  <tr>

   <td width="19">6</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">1</td>

   <td width="19">9</td>

   <td width="19">5</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">6</td>

   <td width="19"><em>7</em></td>

   <td width="19"><em>2</em></td>

   <td width="19">1</td>

   <td width="19">9</td>

   <td width="19">5</td>

   <td width="19"><em>3</em></td>

   <td width="19"><em>4</em></td>

   <td width="19"><em>8</em></td>

  </tr>

  <tr>

   <td width="19"> </td>

   <td width="19">9</td>

   <td width="19">8</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">6</td>

   <td width="19"> </td>

   <td width="19"><em>1</em></td>

   <td width="19">9</td>

   <td width="19">8</td>

   <td width="19"><em>3</em></td>

   <td width="19"><em>4</em></td>

   <td width="19"><em>2</em></td>

   <td width="19"><em>5</em></td>

   <td width="19">6</td>

   <td width="19"><em>9</em></td>

  </tr>

  <tr>

   <td width="19">8</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">6</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">3</td>

   <td width="19">8</td>

   <td width="19"><em>5</em></td>

   <td width="19"><em>9</em></td>

   <td width="19"><em>7</em></td>

   <td width="19">6</td>

   <td width="19"><em>1</em></td>

   <td width="19"><em>4</em></td>

   <td width="19"><em>2</em></td>

   <td width="19">3</td>

  </tr>

  <tr>

   <td width="19">4</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">8</td>

   <td width="19"> </td>

   <td width="19">3</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">1</td>

   <td width="19">4</td>

   <td width="19"><em>2</em></td>

   <td width="19"><em>6</em></td>

   <td width="19">8</td>

   <td width="19"><em>5</em></td>

   <td width="19">3</td>

   <td width="19"><em>7</em></td>

   <td width="19"><em>9</em></td>

   <td width="19">1</td>

  </tr>

  <tr>

   <td width="19">7</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">2</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">6</td>

   <td width="19">7</td>

   <td width="19"><em>1</em></td>

   <td width="19"><em>3</em></td>

   <td width="19"><em>9</em></td>

   <td width="19">2</td>

   <td width="19"><em>4</em></td>

   <td width="19"><em>8</em></td>

   <td width="19"><em>5</em></td>

   <td width="19">6</td>

  </tr>

  <tr>

   <td width="19"> </td>

   <td width="19">6</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">2</td>

   <td width="19">8</td>

   <td width="19"> </td>

   <td width="19"><em>9</em></td>

   <td width="19">6</td>

   <td width="19"><em>1</em></td>

   <td width="19"><em>5</em></td>

   <td width="19"><em>3</em></td>

   <td width="19"><em>7</em></td>

   <td width="19">2</td>

   <td width="19">8</td>

   <td width="19"><em>4</em></td>

  </tr>

  <tr>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">4</td>

   <td width="19">1</td>

   <td width="19">9</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">5</td>

   <td width="19"><em>2</em></td>

   <td width="19"><em>8</em></td>

   <td width="19"><em>7</em></td>

   <td width="19">4</td>

   <td width="19">1</td>

   <td width="19">9</td>

   <td width="19"><em>6</em></td>

   <td width="19"><em>3</em></td>

   <td width="19">5</td>

  </tr>

  <tr>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">8</td>

   <td width="19"> </td>

   <td width="19"> </td>

   <td width="19">7</td>

   <td width="19">9</td>

   <td width="19"><em>3</em></td>

   <td width="19"><em>4</em></td>

   <td width="19"><em>5</em></td>

   <td width="19"><em>2</em></td>

   <td width="19">8</td>

   <td width="19"><em>6</em></td>

   <td width="19"><em>1</em></td>

   <td width="19">7</td>

   <td width="19">9</td>

  </tr>

 </tbody>

</table>

Unsolved Sudoku                                             Solved Sudoku

Figure 1: Sudoku puzzle from https://en.wikipedia.org/wiki/Sudoku

public String toPrintString(char emptyCellLetter) Return a string representing the current state of the grid. The grid is returned with no spaces between cells, the character emptyCellLetter used for any empty cells, and lines separated by carriage returns (
).

The normal course of operation is for a user to

<ol>

 <li>Create a puzzle using the constructor</li>

 <li>Define the symbols for the grid using setPossibleValues</li>

 <li>Constrain the puzzle by setting some of the cell values using setCellValue</li>

 <li>Solve the puzzle using the solve method</li>

</ol>

<h2>Notes</h2>

<ul>

 <li>You are <strong>not asked to write code </strong>to solve this problem.</li>

 <li>Only write test cases for this problem.</li>

 <li><strong>Do not provide test data for your test cases</strong>. Do provide what the method is expected to return (qualitatively for toPrintString).</li>

 <li>I am looking for distinct test cases. Do not duplicate conditions across cases.</li>

 <li>Ensure that your test case description is short but also clear on what is being tested. Cases where we can’t tell what is being tested will be discarded.</li>

</ul>

<h2>Marking scheme</h2>

<ul>

 <li>List of test cases, assessed based on completeness of coverage for the problem and distinctness of the cases – 5 marks</li>

</ul>

<h1>Problem 2</h1>

<strong>Goal</strong>

Implement a data structure from basic objects.

<h2>Background</h2>

Balanced binary search trees can be tricky to code and expensive to maintain. However, we don’t always need a perfectly balanced tree. We are often content with an approximation to the tree or a heuristic structure that mimics the balanced binary tree.

In this assignment, you will implement a data structure that has the structure of an unbalanced binary search tree, but that is designed to make searches for frequently accessed items happen quickly.

<h2>Problem</h2>

Write a class called SearchTree that accepts and stores ordered keys (Strings for this assignment), and then lets you search to see if a particular key is in the tree. The SearchTree should be programmed as an <em>unbalanced </em>binary search tree. New keys are added to the bottom of the tree, maintaining the structure of a binary search tree. Keys should only be stored in the tree once.

A counter is stored along with each key to keep track of how many previous times a key has been accessed. When a key is accessed (i.e. searched for), its counter is increased. If a key’s count is higher than its parent in the tree, then this key is moved up one level in the tree and its parent is moved down a level. More details on this follow.

The public methods of the SearchTree class are as follows:

SearchTree( ) Constructor.

boolean add(String key) Add the key to the tree. Return true if added. Return false if already in the tree or some problem occurs.

int find(String key) Search for key in the tree. If found, return the depth of the node in the tree (Note: the root node has depth 1). If not found or if some error happens, return 0.

void reset() Change all of the counters for searches in the tree to 0.

String printTree() Create a string of the tree’s content. For each key in the tree (reported in sorted order), print the key, a space, and then the depth of the node in the tree. Separate each key with a carriage return (
). Return a null string if any error occurs.

<h2>find operation</h2>

Searching in a binary search tree finds information that is closer to the root of the tree faster than information that is lower in the tree. Our find method will move items that we search for frequently closer to the root of the tree so that we can find them more quickly in later searches.

Suppose that we have a node with key egg and a child node carrot (see fig. 2). We have searched for egg twice and carrot once. When we search for carrot again, we increment its count to 2. When we search for carrot one more time, its count now becomes 3, which is more than its parent egg, so we want to move carrot up the tree by one level. Figure 2 shows how the tree is reshaped around this move. This reshaping must preserve the structure of the binary search tree. A consequence of the reshaping is that the sibling of carrot and all its descendants become further from the root.

The case where the searched node is the right child of the parent is symmetric.

A node is moved up at most one level per search, even if its new parent has smaller count than it.

<strong>Inputs</strong>

All the inputs will be determined by the parameters used in calling your methods.

<strong>Assumptions</strong>

No special assumptions provided for this assignment.

<h2>Constraints</h2>

<ul>

 <li><strong>You may not use any data structures from the Java Collection Framework, including ArrayLists.</strong></li>

 <li>If in doubt for testing, I will be running your program on cs.dal.ca. Correct operation of your program shouldn’t rely on any packages that aren’t available on that system.</li>

 <li>String comparisons should <strong>not </strong>be case sensitive.</li>

</ul>

<h2>Notes</h2>

<ul>

 <li>Start with some basic methods. Get add and search (without the changes to the data structure) working.</li>

 <li>Your nodes for the binary tree will likely benefit from having a reference to the parent node. The root of the tree will have a null value for its parent.</li>

</ul>

↓find(“carrot”)

↓find(“carrot”)

Figure 2: Sequence of find operations for carrot that eventually shift the tree structure

<h2>Marking scheme</h2>

<ul>

 <li>Documentation (internal and external)</li>

 <li>Program organization, clarity, modularity, style</li>

 <li>Ability to search for an item in the tree correctly</li>

 <li>Ability to add an item to the bottom of the tree correctly</li>

 <li>Ability to change the structure of the tree as we search for the same item repeatedly</li>

 <li>Ability to reset the counts for the nodes</li>

 <li>Ability to print the tree</li>

</ul>

<h2>Test cases</h2>

Input Validation

<ul>

 <li>Send a null string to the add method</li>

 <li>Send an empty string to the add method</li>

 <li>Send a null string to the add method</li>

 <li>Send a null string to the find method</li>

</ul>

Boundary Cases

<ul>

 <li>Add a string of 1 character</li>

 <li>Add a long string</li>

 <li>Find a string of 1 character</li>

 <li>Find a long string</li>

 <li>Reset an empty tree</li>

 <li>Reset a tree with 1 node</li>

 <li>Reset a big tree</li>

 <li>Print an empty tree</li>

 <li>Print a tree with 1 node</li>

 <li>Print a big tree</li>

</ul>

Control Flow

<ul>

 <li>add

  <ul>

   <li>Add to an empty tree</li>

   <li>Add to a tree with 1 node</li>

   <li>Add strings in alphabetical order</li>

   <li>Add strings in reverse alphabetical order</li>

   <li>Add a smallest string</li>

   <li>Add a largest string</li>

   <li>Add a string that forces each of the following search sequences:</li>

  </ul></li>

</ul>

∗ Left child then left child

∗ Left child then right child ∗ Right child then left child

∗ Right child then right child

<ul>

 <li>Add an item that is already in the tree</li>

</ul>

<ul>

 <li>find

  <ul>

   <li>Find in an empty tree</li>

   <li>Find in a tree with 1 node</li>

   <li>Find the smallest string in the tree</li>

   <li>Find the largest string in the tree</li>

   <li>Find a middle string</li>

   <li>Search for an item that requires us to follow:</li>

  </ul></li>

</ul>

∗ Left child then left child

∗ Left child then right child ∗ Right child then left child

∗ Right child then right child

<ul>

 <li>Find an item that is in the tree</li>

 <li>Find an item that is not in the tree</li>

</ul>

<ul>

 <li>reset

  <ul>

   <li>Covered under boundary cases</li>

  </ul></li>

 <li>printTree

  <ul>

   <li>Some covered under boundary cases</li>

   <li>Print a tree that is a linked list</li>

   <li>Print a tree that has many levels and has nodes with both right and left children</li>

  </ul></li>

</ul>

Data Flow

<ul>

 <li>Call find before calling add (mentioned earlier for empty tree)</li>

 <li>Call reset before calling add (mentioned earlier for empty tree)</li>

 <li>Call printTree before calling add (mentioned earlier for empty tree)</li>

 <li>Call reset twice in a row</li>

 <li>Call find for a string not in the tree, add it to the tree, then find it again</li>

</ul>