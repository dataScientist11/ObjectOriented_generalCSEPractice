# Interview Submission
## Jobin Thomas
## Udacity Machine Learning Nanodegree


1. The goal for the problem, was to classify if one word is an anagram of the second word. In this case, s is the original word and t is the anagram. I iterate over the anagram and make sure it is contained in the original word. If it is not contained, then I set the return variable found as false and thereby completing the algorithm. Else if it is contained, I convert the anagram into a list and delete the iterating letter from that list. The loop is then repeated. If the found variable is not changed to False, the loop will complete and the function returns True.
2. The goal of this problem was to find the longest palindrome in a string parameter. I use a double for loop to iterate through all combination pieces of the string parameter. If a string piece equals the same string piece inversed, I append that to the possibleChoices array. I return the maximum length string in that array. If there are no strings in possibleChoices, meaning no palindromes in the original string parameter, the function returns 'none found'.
3. Next I find the minimum spanning tree using the prims algorithm. A minimum spanning tree is defined to reach every vertex, has a minimum total weight and there are no cycles in the connection of vertexes. Prims does this by choosing a random vertex and choosing the cheapest edge available that does not create cycles in the vertex connections. In my representation of the prims algorithm, first I created empty lists chosenEdges and chosenVertex. Next I append a random vertex from the keys of the dictionary which contains the 1st vertex as the key, and the 2nd vertex and edge as values for that key. Afterwards, I create a weightTable which sorts the dictionary, into a list. This makes it easier to work with. Next I make a sorted list of all vertexes so that the coming while loop can check and know when the algorithmic iterations can be stopped. Furerthermore inside this while loop, the algorithm iterates through each vertex in the weightTable checking if only one of two, of the vertex set, is contained in the chosenVertexes. This is xor. If conditions are met, the edge is appended and the new vertex is added in order to chosenVertex. The algorithm loop breaks the for loop and it is able to start again at the beginning of the while loop. When chosenVertex equals the completeVertexes, the prims algorithm is now complete and all edges that need to be selected have been selected. The chosen selection is converted back to dictionary form to meet function specifications and printed.
4. I'm still having trouble with this algorithm. The goal is to use two classes to represent the node and the tree. Although I'm having a hard time converting the adjacency matrix into the tree object. Are there any pointers that can help me lead to the solution? I attached an image of the tree I'm using for your convenience. After making the tree object, I would call my lca function which finds the least common denominator. This function returns a node if the value contained is between n1 and n2. This is also an indirect definition of the lowest common ancestor in a binary search tree. If it is not between n1 and n2, it moves onto a child node. More specifically, the right child node if the value is less than the minimum of n1 and n2. Likewise, the left child node if the value is more than the maximum of n1 and n2. 
5. Similar to number 4, I solved this algorithm by creating a node class and then an linkedlist class which contains the previous nodes. Although the user never has to touch the node class, since the linkedlist class calls it every time. I made an array that the function makeLinked creates using the LinkedList class. Next the function getMth finds the total size of the linked list and then subtracts m from it, into the variable newIndex. To conclude the algorithm, the algorithm iterates through the linked list newIndex times and returns the data in that node.

# 4. Revision

> def getChildren(Tree, node):  # read the row in the Tree that belongs to the node, checking each spot for a child
>
    > &nbsp; for position in Tree[node]:
        >
        > &nbsp;&nbsp;if position == 1:
        >
                    > &nbsp;&nbsp;&nbsp;&nbsp;you found a child node, now insert it!

I have a similar method to the code above and it's located in class tree under method table. Although it gives me an error saying 'RuntimeError: maximum recursion depth exceeded'. 

# 5. Revision
Just a quick tweak here - the code should be expecting to be handed the head node of a linked list as ll, not an actual list. All you need to do here is tweak your code to accept the root node, and build the list from there!

I'm confused on how to instantiate an object outside the function. Can you show me an example how?  

