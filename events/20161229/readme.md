
This practice set has 3 problems in it and lasts 3 weeks (until Dec 31) - you submit solutions (a single java file) to individual problems
Problem A. Duck .... Duck ..... Goose ?  
duck, duck, goose works such that one person advances around the exterior of a circle of friends touching the top of their heads and saying duck, eventually they decide to call someone a goose and a race and general dislike of one another ensues. 
Lara has difficulty tapping people on the head and saying duck, and so she often misses a number of people as she advances around the circle. As an example she may only tap every third person on the head and say duck, in general let's say Lara taps every k'th person on the head and says duck. Lara’s teacher Jordan informs her to touch everyone's head and say duck. Lara misunderstands and thinks Jordan is telling her that she must continue her current practice of touching every k'th person  until she has touched everyone's head. Lara continues walking around the circle touching every k'th person's head going round and round the circle. Sometimes she eventually touches everyone's head and other times there are some people that are always left out. Lara would like to know ahead of time on which loop of the circle she will have tapped everyone's head or if she'll continue forever and still not touch everyone.
As an example if k = 1 (that is Lara touches each person in a row without skipping anyone) then obviously she'll reach everyone on the first loop of the circle.
If k = 2 it is a bit more complicated: Lara will touch every second person as she walks around the circle of people - if there's 4 people in the circle, then Lara will never touch everyone.
 
              L
              1 
        4         2
              3

If k = 2 then Lara will tap the 1st person's head but then skip the 2nd person and tap the 3rd person, then skip the 4th person again and once again tap the 1st person ... 
Assume that Lara always starts her count at the first person, so if k = 3 she will tap the 1st person’s head first and then the 4th person’s head (provided there is a 4th person).
You will output the iteration around the circle on which Lara will have touched everyone’s head - or -1 if she’ll never reach some people. 
Input:
2 positive integers k and n on the same line separated by a space ( 1 <= k <= n <= 10000). Where k represents how often Lara calls duck - 5 indicates she calls duck every 5th person. n is the number of people in the circle. Lara always starts tapping with the first person in the circle.
Output:
A single number representing the iteration of the circle on which Lara will have called duck for everyone in the circle at least once and  -1 if Lara will never call duck for all people.
Examples:
Input 1 (in1.txt):
2 4
Output 1:
-1
Input 2 (in2.txt):
2 3
Output 2:
2
Estimated difficulty:  1 x Bill Gates


Problem B
Travel Trouble-o
Trivague-o offers flights to and from destinations around the world. They find and piece together the cheapest flights for you to reach your destination. However often times a terrible problem occurs - they introduce a cycle to one direction of your trip. For example suppose you want to fly from Charlottetown to Paris. Trivague-o may discover that there is a flight from Charlottetown to Toronto that goes through Montreal, and then a flight from Toronto to Paris that again goes through Montreal. This introduces a cycle into your trip - namely montreal - toronto - montreal.  Trivague-o would like to avoid the embarrassment of offering you trips which include a cycle. Your goal is to read in a list of directed origin:destination pairs (edges) and determine if there is any path (combination of edges) leading to a cycle.  
The input consists of first a number N (1 <= N <= 100) on a single line followed by N lines of origin:destination edges (a colon separates the origin and destination). As follows:
6
Charlottetown:New York
New York:Boston
San Francisco:New Orleans
Boston:Charlottetown
San Francisco:Seattle
Seattle:Toronto

The output is either TRUE or FALSE depending on whether a cycle exists (TRUE) or not (FALSE).
For this example because Charlottetown -> New York, New York->Boston, Boston -> Charlottetown forms a cycle then the output is TRUE. 

Estimated Difficulty: 2 x Dishevelled Trivague-o guys



Problem C 
Dominating Dominoes
This problem is unrelated to pizza - a domino is a playing piece with numbers at each end (see example photo of two dominoes). 
Dominique has a bunch of dominoes and he likes to lay them end to end such that the number on one end of a domino matches up with the starting number on the next tile he lays. That is if Dominique has two dominoes as shown in the picture, one with 1 and 5 and the other with 1 and 3, then Dominique lays the dominoes end to end such that the 1's are next to each other.  Thus the numbers may be in order 5 1, 1 3.  Note that either end of the domino tile can be considered the starting end.
Dominique has a big problem on his hands - namely once he gets a large set of dominos he has no idea if he'll be able to lay ALL his dominoes down according to how he likes to always follow a tile that ends in one number with a new tiles that starts with the same number and not have any dominoes left over at the end. Create a program to determine if a given set of dominoes can all be laid according to Dominique's scheme.
The input has on the first line a number N (1 <= N <= 10) representing the number of dominoes to follow on the next N lines. A domino is represented by 2 numbers each between 1 and 6 inclusive. Remember a single domino can be turned such that either direction is the starting side.
Sample input:
3
1 3
1 4
1 3
The output is either TRUE or FALSE depending on whether Dominique can lay the dominoes end to end while always matching numbers and have no dominoes left over.
Sample output:
TRUE
(because 1 3, 3 1, 1 4 provides one way to lay all the dominoes according to the rules).
Another example
Sample input
3 
1 4
5 2
2 2
Sample output:
FALSE
(because there is no way to lay all of the dominos according to Dominique's scheme)

Estimated Difficulty 3 x Q*bert




Hints and Tips:
A) Remember that you’ll read everything from Standard input (that’s System.in in Java) and write everything to standard output (that’s System.out in java). Thus your program will run as java MyProgram < input1.txt if you are running your program with input1.txt as the input from the command line. But you will just read everything in your program from System.in (just like you would for  keyboard input - no specific fileio).
B) While you've been given a few sample input files - keep in mind there may be other input files used to test your solutions.
Made with the new Google Sites, an effortless way to create beautiful sites.	Create a siteReport abuse

