# Linked Lists
## Singly Linked List
A data structure consisting of nodes, each with a value and a pointer to the next node in a linked list. Typically stored in **value** and **next** properties.
## Doubly Linked List
Similar to a singly linked list except that each node also has a pointer to the previous node, stored in the **prev** property.
## circular Linked List
A linked list that has no clear head of tail, because the "tail" points to the "head", forming a closed circle. It can be either a **singly circular linked list** or a **doubly circular linked list**.

Linked list vs array: difference is how it's stored in memory. Array con: you have to allocate back to back memory slots in the memory canvas, and those memory slots may not always be available. contrarily, linked list nodes can be stored anywhere in the memory canvas, and they can point to another memory slot that isn't contiguous because the pointer indicates a memory address. The node in a sll takes two slots: one for the value and one for next. In the tail, the next will indicate it doesn't have to go anywhere else.

Array elements are stored back-to-back in memory.
LL elements are not stored back-to-back: they can be anywhere in memory.
Note that the typical representation of a LL - 3->1->4->2 - doesn't actually visually indicate how the LL is stored in memory. 

Things you can do with LLs mimic the actions you can perform on arrays, such as append, traverse, pop, etc. In an array, you can access a value using the index. Accessing values is not quite as simple in the case of LLs. In the code, you basically just know the head of the LL, so if you want to find the value of the node at index 2 for example, you have to traverse the LL starting at the head, then going to the second node, then the third. 
Thus, to get (access) a value: O(i)T, O(1)S
        - why O(i) time complexity? Because you will move through the LL the number of times as the "index" you want.
    set: O(i)T, O(1)S
        -To set a value you have to get it, thus set also has time complexity O(i).
    initializing a LL: O(N)ST
    copy: O(N)ST
    traverse: O(N)T, O(1)S
    insertion & deletion: 
        - in an array you have to shift every element if you're inserting something, so it's much simpler in a LL bc all you have to do is create a new node and change the pointer of the node before it, making it constant time. If you're adding to the head, it's constant time.
        - If you want, you can also create a variable pointing to the tail of a LL. If you did this, it's constant time; otherwise, it's O(N) time to insert after the tail (thus making a new tail).
        - To go in the middle it's O(i) ??
    
A node in a DLL takes up 3 memory slots: value, next, prev


Node class with next and prev property
In DLLs you almost always have a reference to the tail so you can start from the end and move backwards. Since you can't move backwards in a SLL, it's optional.