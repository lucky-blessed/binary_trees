Binary trees

Resources
Read or watch:

Binary tree (note the first line: Not to be confused with B-tree.)
Data Structure and Algorithms - Tree
Tree Traversal
Binary Search Tree
Data structures: Binary Tree
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

General
What is a binary tree
What is the difference between a binary tree and a Binary Search Tree
What is the possible gain in terms of time complexity compared to linked lists
What are the depth, the height, the size of a binary tree
What are the different traversal methods to go through a binary tree
What is a complete, a full, a perfect, a balanced binary tree

Requirements
General
Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
All your files should end with a new line
A README.md file, at the root of the folder of the project, is mandatory
Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
You are not allowed to use global variables
No more than 5 functions per file
You are allowed to use the standard library
In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
The prototypes of all your functions should be included in your header file called binary_trees.h
Don’t forget to push your header file
All your header files should be include guarded

More Info
Data structures
Please use the following data structures and types for binary trees. Don’t forget to include them in your header file.

Basic Binary Tree


Binary Search Tree
typedef struct binary_tree_s bst_t;
AVL Tree
typedef struct binary_tree_s avl_t;
Max Binary Heap
typedef struct binary_tree_s heap_t;
Note: For tasks 0 to 23 (included), you have to deal with simple binary trees. They are not BSTs, thus they don’t follow any kind of rule.

Print function
To match the examples in the tasks, you are given this function

This function is used only for visualization purposes. You don’t have to push it to your repo. It may not be used during the correction

Tasks
0. New node
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that creates a binary tree node

Prototype: binary_tree_t *binary_tree_node(binary_tree_t *parent, int value);
Where parent is a pointer to the parent node of the node to create
And value is the value to put in the new node
When created, a node does not have any child
Your function must return a pointer to the new node, or NULL on failure

Repo:

GitHub repository: binary_trees
File: 0-binary_tree_node.c
     
1. Insert left
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that inserts a node as the left-child of another node

Prototype: binary_tree_t *binary_tree_insert_left(binary_tree_t *parent, int value);
Where parent is a pointer to the node to insert the left-child in
And value is the value to store in the new node
Your function must return a pointer to the created node, or NULL on failure or if parent is NULL
If parent already has a left-child, the new node must take its place, and the old left-child must be set as the left-child of the new node.

Repo:

GitHub repository: binary_trees
File: 1-binary_tree_insert_left.c
     
2. Insert right
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that inserts a node as the right-child of another node

Prototype: binary_tree_t *binary_tree_insert_right(binary_tree_t *parent, int value);
Where parent is a pointer to the node to insert the right-child in
And value is the value to store in the new node
Your function must return a pointer to the created node, or NULL on failure or if parent is NULL
If parent already has a right-child, the new node must take its place, and the old right-child must be set as the right-child of the new node.

Repo:

GitHub repository: binary_trees
File: 2-binary_tree_insert_right.c
     
3. Delete
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that deletes an entire binary tree

Prototype: void binary_tree_delete(binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to delete
If tree is NULL, do nothing

Repo:

GitHub repository: binary_trees
File: 3-binary_tree_delete.c
     
4. Is leaf
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that checks if a node is a leaf

Prototype: int binary_tree_is_leaf(const binary_tree_t *node);
Where node is a pointer to the node to check
Your function must return 1 if node is a leaf, otherwise 0
If node is NULL, return 0

Repo:

GitHub repository: binary_trees
File: 4-binary_tree_is_leaf.c
     
5. Is root
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that checks if a given node is a root

Prototype: int binary_tree_is_root(const binary_tree_t *node);
Where node is a pointer to the node to check
Your function must return 1 if node is a root, otherwise 0
If node is NULL, return 0

Repo:

GitHub repository: binary_trees
File: 5-binary_tree_is_root.c
     
6. Pre-order traversal
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that goes through a binary tree using pre-order traversal

Prototype: void binary_tree_preorder(const binary_tree_t *tree, void (*func)(int));
Where tree is a pointer to the root node of the tree to traverse
And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
If tree or func is NULL, do nothing

Repo:

GitHub repository: binary_trees
File: 6-binary_tree_preorder.c
     
7. In-order traversal
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that goes through a binary tree using in-order traversal

Prototype: void binary_tree_inorder(const binary_tree_t *tree, void (*func)(int));
Where tree is a pointer to the root node of the tree to traverse
And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
If tree or func is NULL, do nothing

Repo:

GitHub repository: binary_trees
File: 7-binary_tree_inorder.c
     
8. Post-order traversal
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that goes through a binary tree using post-order traversal

Prototype: void binary_tree_postorder(const binary_tree_t *tree, void (*func)(int));
Where tree is a pointer to the root node of the tree to traverse
And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
If tree or func is NULL, do nothing

Repo:

GitHub repository: binary_trees
File: 8-binary_tree_postorder.c
     
9. Height
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that measures the height of a binary tree

Prototype: size_t binary_tree_height(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to measure the height.
If tree is NULL, your function must return 0

Repo:

GitHub repository: binary_trees
File: 9-binary_tree_height.c
     
10. Depth
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that measures the depth of a node in a binary tree

Prototype: size_t binary_tree_depth(const binary_tree_t *tree);
Where tree is a pointer to the node to measure the depth
If tree is NULL, your function must return 0

Repo:

GitHub repository: binary_trees
File: 10-binary_tree_depth.c
     
11. Size
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that measures the size of a binary tree

Prototype: size_t binary_tree_size(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to measure the size
If tree is NULL, the function must return 0

Repo:

GitHub repository: binary_trees
File: 11-binary_tree_size.c
     
12. Leaves
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that counts the leaves in a binary tree

Prototype: size_t binary_tree_leaves(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to count the number of leaves
If tree is NULL, the function must return 0
A NULL pointer is not a leaf

Repo:

GitHub repository: binary_trees
File: 12-binary_tree_leaves.c
     
13. Nodes
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that counts the nodes with at least 1 child in a binary tree

Prototype: size_t binary_tree_nodes(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to count the number of nodes
If tree is NULL, the function must return 0
A NULL pointer is not a node

Repo:

GitHub repository: binary_trees
File: 13-binary_tree_nodes.c
     
14. Balance factor
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that measures the balance factor of a binary tree

Prototype: int binary_tree_balance(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to measure the balance factor
If tree is NULL, return 0

Repo:

GitHub repository: binary_trees
File: 14-binary_tree_balance.c
     
15. Is full
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that checks if a binary tree is full

Prototype: int binary_tree_is_full(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to check
If tree is NULL, your function must return 0

Repo:

GitHub repository: binary_trees
File: 15-binary_tree_is_full.c
     
16. Is perfect
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that checks if a binary tree is perfect

Prototype: int binary_tree_is_perfect(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to check
If tree is NULL, your function must return 0

Repo:

GitHub repository: binary_trees
File: 16-binary_tree_is_perfect.c
     
17. Sibling
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that finds the sibling of a node

Prototype: binary_tree_t *binary_tree_sibling(binary_tree_t *node);
Where node is a pointer to the node to find the sibling
Your function must return a pointer to the sibling node
If node is NULL or the parent is NULL, return NULL
If node has no sibling, return NULL

Repo:

GitHub repository: binary_trees
File: 17-binary_tree_sibling.c
     
18. Uncle
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a function that finds the uncle of a node

Prototype: binary_tree_t *binary_tree_uncle(binary_tree_t *node);
Where node is a pointer to the node to find the uncle
Your function must return a pointer to the uncle node
If node is NULL, return NULL
If node has no uncle, return NULL

Repo:

GitHub repository: binary_trees
File: 18-binary_tree_uncle.c
     
19. Lowest common ancestor
#advanced
Score: 0.0% (Checks completed: 0.0%)
Write a function that finds the lowest common ancestor of two nodes

Prototype: binary_tree_t *binary_trees_ancestor(const binary_tree_t *first, const binary_tree_t *second);
Where first is a pointer to the first node
And second is a pointer to the second node
Your function must return a pointer to the lowest common ancestor node of the two given nodes
If no common ancestor was found, your function must return NULL

Repo:

GitHub repository: binary_trees
File: 100-binary_trees_ancestor.c
     
20. Level-order traversal
#advanced
Score: 0.0% (Checks completed: 0.0%)
Write a function that goes through a binary tree using level-order traversal

Prototype: void binary_tree_levelorder(const binary_tree_t *tree, void (*func)(int));
Where tree is a pointer to the root node of the tree to traverse
And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
If tree or func is NULL, do nothing

Repo:

GitHub repository: binary_trees
File: 101-binary_tree_levelorder.c
     
21. Is complete
#advanced
Score: 0.0% (Checks completed: 0.0%)
Write a function that checks if a binary tree is complete

Prototype: int binary_tree_is_complete(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to check
If tree is NULL, your function must return 0
