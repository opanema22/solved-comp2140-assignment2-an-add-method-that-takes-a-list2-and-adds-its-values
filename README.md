Download Link: https://assignmentchef.com/product/solved-comp2140-assignment2-an-add-method-that-takes-a-list2-and-adds-its-values
<br>
When writing code for this course, <strong>follow the programming standards</strong>, available on this course’s website on UM Learn. Failure to do so will result in the loss of marks.

<strong>What you should implement: </strong>Implement the following algorithms and methods (you can add any necessary private helper methods):

<ol>

 <li><strong>add(): </strong>In the LinkedList class implement an add method that takes a list2 and adds its values (not nodes) to the current list list1. Please consider these points:

  <ul>

   <li>Both lists are circular single linked list.</li>

   <li>Both lists are ordered. Order of list1 must be preserved while adding values from list2.</li>

   <li>The list2 should not change.</li>

  </ul></li>

</ol>

The following three methods are designed to familiarize you with linked list improvements.

<ol start="2">

 <li><strong>convertCircularToOrdinary() </strong>In the LinkedList class convert a circular list to an ordinary linked list (a single linked list without dummy header or trailer).

  <ul>

   <li>The existing linkedList.java class is implemented for a circular linked list.</li>

   <li>This conversion will only change address pointers; we will not rewrite insert or search functions for an ordinary linked list.</li>

   <li>When the function returns, the last pointer of the LinkedList class will point to the first node in the list, and the last node will have a null for the forward (next) node.</li>

  </ul></li>

 <li><strong>convertOrdinaryToCircular() </strong>In the LinkedList class convert an ordinary linked list to a circular linked list.

  <ul>

   <li>This conversion will only change address pointers.</li>

   <li>When the function returns, the last pointer of the LinkedList class will point to the last node in the list, and the last.next will point to the first node of the linked list.</li>

  </ul></li>

 <li><strong>reset()</strong>: Reset the linked list to an empty circular link list.</li>

 <li><strong>addDummies(): </strong>In the LinkedList class add a dummy header and a dummy trailer to the linked list. Use Integer.MIN VALUE and Integer.MAX VALUE as values.</li>

 <li><strong>hasDummies()</strong>: In the LinkedList class check if the linked list has a dummy header with Integer.MIN VALUE and a dummy trailer with Integer.MAX VALUE.</li>

 <li><strong>deleteOddNodes(): </strong>In the LinkedList class delete all nodes that have an odd item value.

  <ul>

   <li>Delete by reassigning pointers.</li>

   <li>Do not create a new linked list.</li>

  </ul></li>

</ol>

Figure 1: An ordinary linked list

The following two methods are designed to show the efficiency of array operations when the data size is fixed.

<ol start="8">

 <li><strong>testInsertion(): </strong>In A1&lt;your last name&gt;&lt;your first name&gt;.java, write a method to insert ’size’ new integers into the list (for example, you can insert a dummy 1 every time), and record the time it takes to complete these insertions.</li>

 <li><strong>testInsertion()(version 2): </strong>In A1&lt;your last name&gt;&lt;your first name&gt;.java, write a method to insert ’size’ new integers into the array (you can insert a dummy 1 every time), and record the time it takes to complete these insertions.</li>

</ol>

Reminder: These two insertion methods are overloaded; they have the same name but different signatures.

<a href="https://www.geeksforgeeks.org/different-ways-method-overloading-java/">(</a><a href="https://www.geeksforgeeks.org/different-ways-method-overloading-java/">https://www.geeksforgeeks.org/different-ways-method-overloading-java/</a><a href="https://www.geeksforgeeks.org/different-ways-method-overloading-java/">)</a>

The following two methods are designed to show the efficiency of Linked Lists when data size changes in time.

<ol start="10">

 <li><strong>insertValue()</strong>: In A1&lt;your last name&gt;&lt;your first name&gt;.java, insert the given value into the link list.</li>

 <li><strong>insertValue() (version 2)</strong>: In A1&lt;your last name&gt;&lt;your first name&gt;.java, insert the given value into the array. If the array size is exceeded, you must create a new array and copy the old array into the new array. Afterwards, insert the new item value to the new array.</li>

</ol>

The following two methods are designed to familiarize you with a well known linked list algorithm.

<ol start="12">

 <li><strong>corrupt()</strong>: In the LinkedList.java write a method that corrupts a given ordinary linked list by changing the last node’s forward pointer (which is supposed to be null) to point to a node at the given index. In Figure 1 a clean list is shown. In Figure 2, its corrupted version is shown. The task in corrupt() is to convert a clean linked list to a corrupted one. The position to corrupt is determined by the line</li>

</ol>

index = r1.nextInt(list1.getSize()/2); which chooses the corruption index from the first half of the linked list.

<ol start="13">

 <li><strong>findCorruption()</strong>: In the LinkedList.java write a method that finds if the linked list contains a loop (This is a popular software interview question).

  <ul>

   <li>In the main class, a sorted list is given as the parameter to this method (for ease of debugging). Do not use the sorted nature of the linked list to detect the corruption.</li>

   <li>Do not store visited nodes to detect a loop. That would be a very lazy solution. If the linked list is big, you would store too much information.</li>

  </ul></li>

</ol>

Figure 2: A corrupted linked list

<strong>Concerns.</strong>

It is not optimal to have hard-coded parameters in your class such as final int list1Size = 1500;

Ideally, your main class should be passed an array of arguments. In this assignment, we are receiving list sizes (list1Size=1500 and list2Size=1300) from the argument array args and parsing them to integers with the following lines.

int list1Size = Integer.parseInt(args[0]); int list2Size = Integer.parseInt(args[1]);

Please avoid magical numbers in your code. There should be only ONE return per method. See the programming standards (under content/course documents) file on UMLearn, and follow the suggestions. Assignments will be graded by considering these standards. Your code must not give any warnings or errors when compiled and run.