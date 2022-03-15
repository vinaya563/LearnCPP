## STACK 

- A linear-data structure that follows LIFO (Last In First Out) principle.
- It is useful when we need to store data in a particular order like... function calls during recursion
- It can be implemented using Array or Linked List. (Each has its own pros and cons. Try thinking yourself)
- Implementation of the basic operations like push, pop, peek etc  provided [here](StacksWithoutSTL.cpp). 

![stack](https://user-images.githubusercontent.com/60391776/155890360-c291d4d6-1427-47f7-abb6-9246ea64e2fd.png)

Applications of stack :

1. Parenthesis Balancing
2. Infix to prefix or postfix conversion
3. To reverse a word or a string
4. _Call stack_ : To store list of functions that are either executing or waiting to be executed during runtime. ( stored in stack in memory)
5. Practical application : (<-)Back button present in a browser pushes the URLs of the visited sites on a stack.

## Balanced parentheses using stack

A parentheses is said to be balanced if each left parenthesis has its respective right parenthesis to match its pair in a well-nested format.

In computer science, valid parentheses(balanced parentheses) are a notation used to simplify expressions written in an operator-precedence parser by allowing the programmer to explicitly mark the operator precedence and associativity of a given expression.

 # What is valid parentheses problem?
  Given a string s containing just the characters '(', ')', '{', '}', '[', and ']', determine if the input string is valid or not.

Note that an input string is valid if:

1)Open brackets must be closed by the same type of brackets
2)Open brackets must be closed in the correct order

 # Algorithm using stack
 
 To solve a valid parentheses problem optimally, you can make use of Stack data structure. Here you traverse through the expression and push the characters one by one inside the stack. Later, if the character encountered is the closing bracket, pop it from the stack and match it with the starting bracket. This way, you can check if the parentheses find their respective pair at the end of the traversal and if not, the parentheses are not valid.
1. Declare stack S.
2. Now traverse the string expression using a pointer. 
    if the current pointer is at opening bracket ('(' or '{' or '[') then push it to stack S.
    else the current pointer is at closing bracket (')' or '}' or ']') then pop from the stack 
        if the popped bracket is the matching opening bracket then brackets are valid 
        else brackets are not valid.

After complete traversal, if there is some starting bracket left in the stack then "not valid"

Hence the code is optimum and the time complexity for performing the operations on stack is O(n) where n is the number of characters present in the given ecxpression

