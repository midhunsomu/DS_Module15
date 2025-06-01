# Ex 3(B) Binary Search Tree
## DATE: 14.03.2025
## AIM:
To write a C function to insert the elements in the binary search tree

## Algorithm
1. Start
2. Check if the current node is NULL; if true, create a new node with the given key.
3. Allocate memory for the new node, set its key, and initialize its left and right children to NULL.
4. If the current node is not NULL, compare the key with the current node's key.
5. If key <= node->key, recursively insert the key into the left subtree and update the left child pointer.
6. If key > node->key, recursively insert the key into the right subtree and update the right child pointer.
7. Return the current node after the insertion.
8. End

## Program:
```
/*
Program to insert the elements in the binary search tree
Developed by: Midhun S
RegisterNumber: 212223240087
*/
/*struct node { int key;
struct node *left, *right;
};*/
struct node* insert(struct node* node, int key)
{
if(node==NULL)
{
struct node* node=(struct node*)malloc(sizeof(struct node)); node->key=key;
node->left=NULL; node->right=NULL; return node;
}
else
{
struct node* cur; if(key<=node->key)
{
cur=insert(node->left,key); node->left=cur;
}
else
{
cur=insert(node->right,key); node->right=cur;
}
return node;
}
}
```

## Output:
![image](https://github.com/user-attachments/assets/7aa7666a-9589-4dcb-8d84-ff3fcf02441d)



## Result:
Thus, the C function to insert the elements in the binary search tree is implemented successfully.
