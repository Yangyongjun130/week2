# 二叉查找树的建立与相关操作
## 二叉查找树的关键性质
二叉查找树的关键性质是：对于树中的每一个结点X，他的左子树中的每一个关键字值都小于X的关键字值，而右子树的每一个关键字结点值都大于X的关键字值。二叉搜索树是满足如下性质的二叉树：即任何一个节点的左子树节点值都小于根节点值，进而又小于其右子树节点的值。所以，二叉搜索树的中序遍历是有序的。接下来主要介绍二叉搜索树的相关操作，包括创建、插入、删除、查找等；其时间复杂度与树的高度成正比，即O(logn)。
## 二叉查找树的插入操作
将某节点(insert_node)插入至以node为根二叉查找树中：
如果insert_node节点值小于当前node节点值：
如果node 有左子树，则递归的将该节点插入至以左子树为根的二叉查找树中。
否则，将node->left赋值为该节点地址。
否则(大于等于的情况):
如果node 有右子树，则递归的将该节点插入至以右子树为根的二叉查找树中。
否则，将node->right赋值为该节点的地址。
## 二叉查找树的搜索操作
查找数值
查找数值value 是否在 二叉查找树中 出现：
如果value 等于当前查找node的节点值，则返回真
如果value节点值小于当前节点node的值：
如果当前节点有左子树，继续在左子树中递归查找该值，否则，返回假；
如果value节点值大于当前节点node的值：
如果当前节点有右子树，继续在右子树中递归查找该值，否则，返回假；
