# Coding Problems<br/>

## 1. Circle Group Detection<br/>
**Problem**: A circle is defined by x-axis position, y-axis position, and a radius. A circle group is a collection of circles that overlap. Given a list of circles, figure out if they belong to a single circle group.<br/>

## 2. Tree Leaf Node Removal<br/>
**Problem**: For a rooted tree with any arbitrary number of children for each node, not necessarily n-ary tree. Remove all the leaf nodes, and store them in a list, this would create new leaf nodes. Repeat until all the nodes are removed. Freshly created leaf nodes (node whose children are removed) should not be removed just after its children are removed, unless there's no other option for us, then we can remove it.<br/>

## 3. Recent Searches Data Structure<br/>
**Problem**: Design a search data structure to store and display recent searches. If a user just clicks the search bar without typing anything, it should return the N most recent searches. Given a search string it should save the search and also return the N most recent searches.<br/>

## 4. Minimum Cost Path<br/>
**Problem**: Given a graph or network with weighted edges, find the path between two nodes with the minimum total cost.<br/>

## 5. String Substitution<br/>
**Problem**: Given map {X=>123, Y=456}<br/>
Input: %X%_%Y%<br/>
Output: 123_456<br/>
Given map {USER=>admin, HOME=>/%USER%/home} Input: I am %USER% My home is %HOME% Output: I am admin My home is /admin/home<br/>
USER= bob<br/>
HOME= /home/%USER% should be substituted as : /home/bob ex2:<br/>
home/ %USER% -> /home/bob<br/>
Hello %USER% -> Hello bob!<br/>
ex3:<br/>
The user %USER% is at 50%% -> The user bob is at 50%<br/>

## 6. User Session Count<br/>
**Problem**: You are given a list of user sessions where each user session has start and end times both inclusive. Now, given a value N, find the count of all users at each point in time from [0,N) i.e include 0 but exclude N. Example:<br/>
Input:<br/>
[(0,3), (1,4) ] N=7<br/>
Output:<br/>
0->1<br/>
1->2<br/>
2->2<br/>
3->2<br/>
4->1<br/>

## 7. Cheating Minimization<br/>
**Problem**: A number of students are taking exams in a room. Students sitting adjacent to each other and taking the same exam can cheat. Arrange the students so that cheating opportunities are minimized. I was free to choose input format.<br/>
I chose the input to be a list of length n, denoting n students. The element at index i would indicate the exam student i is taking.<br/>
For example, [1,2,3,1,2,2]<br/>
Student 0 is taking exam 1<br/>
Student 1 is taking exam 2<br/>
Student 2 is taking exam 3<br/>
Student 3 is taking exam 1<br/>
Student 4 is taking exam 2<br/>
Student 5 is taking exam 2<br/>
Output would be a list with the students re-arranged. An acceptable output for the above case would be [1,2,3,2,1,2].<br/>

## 8. Directory File Replacement<br/>
**Problem**: Replace files with directories if all files in directory are specified<br/>
Example input & output:<br/>
allFiles = [<br/>
"a/b/c/d.txt",<br/>
"a/b/c/e.txt",<br/>
"a/b/b.txt",<br/>
"a/b/e.txt",<br/>
"b/c/d.txt"<br/>
]<br/>
subsetFiles = [<br/>
"a/b/c/d.txt",<br/>
"a/b/c/e.txt",<br/>
"a/b/b.txt",<br/>
"b/c/d.txt"<br/>
]<br/>
output=[<br/>
"a/b/c",<br/>
"a/b/b.txt",<br/>
"b"<br/>
]<br/>

## 9. RPC Request Timeout Detection<br/>
**Problem**: You have a stream of rpc requests coming in. Each log is of the form {id, timestamp, type(start/end)}. Given a timeout T, you need to figure out at the earliest possible time if a request has timed out.<br/>
Eg :<br/>
id - time - type<br/>
0 - 0 - Start<br/>
1 - 1 - Start<br/>
0 - 2 - End<br/>
2 - 6 - Start<br/>
1 - 7 - End<br/>
Timeout = 3<br/>
Ans : {1, 6} ( figured out id 1 had timed out at time 6 )<br/>

## 10. Unique Character List<br/>
**Problem**: Give a list of string, where every string in the list is of size 5. Return the list of 5 string such that all the characters in each of the strings are unique<br/>
i.e if we combine all the strings(not nnecessary) we will have 25 unique characters)<br/>
eg<br/>
Input explanation<br/>
List of string with length of 5 each<br/>
intput = ["abcde", "fghij", "klmno", "pqrst", "uvwxy", "zabcd", "apple", "zebra", "ocean", "quick", "world", "jumps", "foxes", "liver"]<br/>

## 11. Odd-Even Element Sorting<br/>
**Problem**: sort all odd elements and leave even elements as it is at their original position<br/>

## 12. Earnings Maximization Schedule<br/>
**Problem**: You work as a consultant and have clients in cityA and cityB. On a given day, say i, you can either work in cityA and make Ai dollars or you can work in cityB and make Bi dollars. You can also spend the day traveling between cityA and cityB in which case your earnings that day are 0.<br/>
Given Al,A2, ....An and B1, B2,....., Bn, return a schedule S of N days which maximizes your earnings, where S is a string of length N, and Si = A/B/T where A means work in cityA, B means work in cityB T means travel on day i. You can start either in cityA or cityB. Example1: A = [23, 4,5 ,101] B = [21,1,10, 100] The optimal schedule S here would be ->"ATBB"<br/>
Example 2:<br/>
A[25,10,15,10,70] B = [5,5,50,5,30] The optimal schedule S here would be-> "ATBTA"<br/>

## 13. Salary Comparison Among Managers<br/>
**Problem**: Give the count of managers who has salary less than average salary of direct and indirect employees<br/>
Example:<br/>
A->B, A->C, A->D, B->E<br/>
Salaries<br/>
A = 50000<br/>
B = 20000<br/>
C = 10000<br/>
D = 10000<br/>
E = 25000<br/>
Answer: 1<br/>
Explanation: A is the manager of direct employees B, C, D and indirect employee E so avg. is 16,250 and B = 20000 < E = 25000 so answer is B<br/>

## 14. Robot Navigation<br/>
**Problem**: There is a robot at location (0, 0) of a 10x10 grid of tiles. Each tile can be one of 8 different colors: (0, 1, ... 7). There is a star at a known location (marked with the color -1) on the grid. You can program the robot by giving it a lookup table of color to direction. The robot will sense the color of the tile it is currently on, and move in the direction (up, down, left, or right) specified by the lookup table you provided. Output a lookup table that guides the robot to the star, if such a table is possible.<br/>
Small example grid: [[(0), 1, 0, 0], [3, 2,-1, 3], [0, 0, 0, 2], [0, 0, 0, 4]]<br/>

## 15. Stream Mean Calculation<br/>
**Problem**: There is a stream of integers. Every time you see a new element in the stream, return the mean value of the last N elements, excluding the largest K elements.<br/>
Example:<br/>
N=5<br/>
K=2<br/>
elements so far = [20, 2, -2, 0, 10, 1, 5, -2, 0]<br/>
last N elements: [10, 1, 5, -2, 0] largest K elements: [10, 5]<br/>
result = (1+(-2)+0)/3 = -0.3333333<br/>

## 16. Longest Increasing Subsequence Length<br/>
**Problem**: Find the length of longest increasing subsequence such that the difference between consecutive elements in LIS is an increasing sequence<br/>
Example :<br/>
nums -> 1 2
