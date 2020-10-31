⇧
Javatpoint Logo

Home
Data Structure
C
C++
C#
Java
SQL
HTML
CSS
JavaScript
Ajax
Android
Cloud
Design Pattern
Quiz
Projects
Interview Q
Comment
Forum

DS Tutorial
DS TutorialDS IntroductionDS AlgorithmAsymptotic AnalysisDS PointerDS Structure
DS Array
DS Array2D Array
DS Linked List
Linked ListDoubly Linked ListCircular Linked ListCircular Doubly ListSkip list in DS
DS Stack
DS StackArray ImplementationLinked List Implementation
DS Queue
DS QueueArray RepresentationLinked List RepresentationCircular QueueDeque
DS Tree
DS TreeBinary TreeBinary Search TreeAVL TreeB TreeB+ Tree
DS Graph
DS GraphGraph ImplementationBFS AlgorithmDFS AlgorithmSpanning Tree
DS Searching
Linear SearchBinary Search
DS Sorting
Bubble SortBucket SortComb SortCounting SortHeap SortInsertion SortMerge SortQuick SortRadix SortSelection SortShell SortBitonic SortCocktail SortCycle SortTim Sort
Differences
Linear vs non-linearArray vs linked listStack vs queueJavaTpoint
next →← prev
AVL Tree
AVL Tree is invented by GM Adelson - Velsky and EM Landis in 1962. The tree is named AVL in honour of its inventors.

AVL Tree can be defined as height balanced binary search tree in which each node is associated with a balance factor which is calculated by subtracting the height of its right sub-tree from that of its left sub-tree.

Tree is said to be balanced if balance factor of each node is in between -1 to 1, otherwise, the tree will be unbalanced and need to be balanced.

Balance Factor (k) = height (left(k)) - height (right(k))
If balance factor of any node is 1, it means that the left sub-tree is one level higher than the right sub-tree.

If balance factor of any node is 0, it means that the left sub-tree and right sub-tree contain equal height.

If balance factor of any node is -1, it means that the left sub-tree is one level lower than the right sub-tree.

An AVL tree is given in the following figure. We can see that, balance factor associated with each node is in between -1 and +1. therefore, it is an example of AVL tree.

AVL Tree
Complexity
Algorithm	Average case	Worst case
Space	o(n)	o(n)
Search	o(log n)	o(log n)
Insert	o(log n)	o(log n)
Delete	o(log n)	o(log n)
Operations on AVL tree
Due to the fact that, AVL tree is also a binary search tree therefore, all the operations are performed in the same way as they are performed in a binary search tree. Searching and traversing do not lead to the violation in property of AVL tree. However, insertion and deletion are the operations which can violate this property and therefore, they need to be revisited.

SN	Operation	Description
1	Insertion	Insertion in AVL tree is performed in the same way as it is performed in a binary search tree. However, it may lead to violation in the AVL tree property and therefore the tree may need balancing. The tree can be balanced by applying rotations.
2	Deletion	Deletion can also be performed in the same way as it is performed in a binary search tree. Deletion may also disturb the balance of the tree therefore, various types of rotations are used to rebalance the tree.
Why AVL Tree?
AVL tree controls the height of the binary search tree by not letting it to be skewed. The time taken for all operations in a binary search tree of height h is O(h). However, it can be extended to O(n) if the BST becomes skewed (i.e. worst case). By limiting this height to log n, AVL tree imposes an upper bound on each operation to be O(log n) where n is the number of nodes.

AVL Rotations
We perform rotation in AVL tree only in case if Balance Factor is other than -1, 0, and 1. There are basically four types of rotations which are as follows:

L L rotation: Inserted node is in the left subtree of left subtree of A
R R rotation : Inserted node is in the right subtree of right subtree of A
L R rotation : Inserted node is in the right subtree of left subtree of A
R L rotation : Inserted node is in the left subtree of right subtree of A
Where node A is the node whose balance Factor is other than -1, 0, 1.

The first two rotations LL and RR are single rotations and the next two rotations LR and RL are double rotations. For a tree to be unbalanced, minimum height must be at least 2, Let us understand each rotation

1. RR Rotation
When BST becomes unbalanced, due to a node is inserted into the right subtree of the right subtree of A, then we perform RR rotation, RR rotation is an anticlockwise rotation, which is applied on the edge below a node having balance factor -2

AVL Rotations
In above example, node A has balance factor -2 because a node C is inserted in the right subtree of A right subtree. We perform the RR rotation on the edge below A.

2. LL Rotation
When BST becomes unbalanced, due to a node is inserted into the left subtree of the left subtree of C, then we perform LL rotation, LL rotation is clockwise rotation, which is applied on the edge below a node having balance factor 2.

AVL Rotations
In above example, node C has balance factor 2 because a node A is inserted in the left subtree of C left subtree. We perform the LL rotation on the edge below A.

3. LR Rotation
Double rotations are bit tougher than single rotation which has already explained above. LR rotation = RR rotation + LL rotation, i.e., first RR rotation is performed on subtree and then LL rotation is performed on full tree, by full tree we mean the first node from the path of inserted node whose balance factor is other than -1, 0, or 1.
