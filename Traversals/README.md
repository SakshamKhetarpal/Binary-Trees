# DFS Traversals
### 1) Recursive Preorder Traversal
 ```cpp
void preorder(node *root)
{
    if (root == nullptr)
    {
        return;
    }
    cout << root->data << " ";
    preorder(root->left);
    preorder(root->right);
}
```
### 2) Recursive Inorder Traversal
 ```cpp
void inorder(node *root)
{
    if (root == nullptr)
    {
        return;
    }
    inorder(root->left);
    cout << root->data << " ";
    inorder(root->right);
}
```
### 3) Recursive Postorder Traversal
 ```cpp
void preorder(node *root)
{
    if (root == nullptr)
    {
        return;
    }
    cout << root->data << " ";
    preorder(root->left);
    preorder(root->right);
}
```

# BFS Traversal
### 1) Level Order Traversal
```cpp
void level_order(node *root)
{
    queue<node *> q;
    if (root == nullptr)
    {
        cout << "Null tree";
    }
    q.push(root);
    while (!q.empty())
    {
        int x = q.size();
        while (x--)
        {
            node *current = q.front();
            q.pop();
            cout << current->data << " ";
            if (current->left)
            {
                q.push(current->left);
            }
            if (current->right)
            {
                q.push(current->right);
            }
        }
        cout << endl;
    }
}
```
