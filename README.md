Download Link: https://assignmentchef.com/product/solved-cs-2123-data-structures-programming-project-3
<br>
In this project, we will be implementing the functionality of the forward/back buttons of a web browser.  For example, if we go to: <a href="https://www.google.com/">www.google.com</a><a href="https://www.google.com/">,</a> then to <a href="https://www.yahoo.com/">www.yahoo.com</a><a href="https://www.yahoo.com/">,</a> and then to <a href="http://www.utsa.edu/">www.utsa.edu</a><a href="http://www.utsa.edu/">,</a> the browser would store these websites in order in memory.  If we want to go back, then we would be taken back to yahoo.  If we then clicked forward, we would then be taken back to utsa.edu.

We will call the data structure to handle the functionality a <strong>BrowserList.  </strong>A browser list will consist of a <strong>DoublyLinkedList</strong>, where each node in the linked list will store a webpage URL and will have a pointer to the node containing the webpage that comes before it in the list and a pointer to the node containing the webpage that comes after it.  The BrowserList will also have a pointer the node containing the URL of the webpage we are currently viewing.




<strong>Example: </strong>

We first create an empty BrowserList which will contain an empty DoublyLinkedList.




<ul>

 <li>Then we go to <a href="https://www.google.com/">google.com</a><a href="https://www.google.com/">:</a></li>

</ul>




<ul>

 <li>Then we go to <a href="https://www.yahoo.com/">yahoo.com</a><a href="https://www.yahoo.com/">:</a></li>

</ul>




<ul>

 <li>Then we go to <a href="http://www.utsa.edu/">utsa.edu</a><a href="http://www.utsa.edu/">:</a></li>

</ul>




<ul>

 <li>Then we go “back”:</li>

</ul>




<ul>

 <li>Then we go “forward”:</li>

</ul>
















<strong>Files provided in the project: </strong>

<ul>

 <li>h. This file contains the structs needed for the DoublyLinkedList class as well as the prototypes for several functions that you will need to implement.  In particular you need to implement the following functions in the file DoublyLinkedList.c:

  <ol>

   <li><strong>DoublyLinkedList newDoublyLinkedList()</strong> which should allocate the memory for a new doubly linked list, initialize the variables, and return the address.</li>

   <li><strong>void freeDoublyLinkedList(DoublyLinkedList list)</strong> which should free the linked list (including any nodes currently in the list).</li>

   <li><strong>NodeDL *allocateNode(Element value) </strong>which should allocate memory for a new node, store “value” inside this node, and return the address of the node.</li>

   <li><strong>void append(DoublyLinkedList list, Element value)</strong> which should add a new node (which stores value) to the end of the list. Notice that often one would want to insert into the middle of a linked list, but for this project it suffices to only insert at the end of a linked list.</li>

  </ol></li>

</ul>




<ul>

 <li>h. This file contains the struct for the BrowserList as well as the prototypes for the functions that you will need to implement.  In particular you need to implement the following functions in the file BrowserList.c:

  <ol>

   <li><strong>BrowserList newBrowserList()</strong> which allocates the memory for a new BrowserList, initializes its variables, and returns its address.</li>

   <li><strong>void freeBrowserList(BrowserList browserList) </strong>which frees the memory used for the BrowserList (including its DoublyLinkedList).</li>

   <li><strong>void goToURL(BrowserList browserList, Element element) </strong>which will add a node in the DoublyLinkedList that stores element after pCurrentURL (any nodes that were in the list after pCurrentURL should be removed from the list) and updates pCurrentURL to point to the new node.</li>

   <li><strong>int back(BrowserList browserList) </strong>which moves pCurrentURL “back” one page. It returns TRUE if this completed successfully and returns false otherwise (e.g. the node doesn’t exist).</li>

   <li><strong>int forward(BrowserList browserList) </strong>which moves pCurrentURL “forward” one page. It returns TRUE if this completed successfully and returns false otherwise (e.g. the node doesn’t exist).</li>

   <li><strong>void printBrowserList(BrowserList browserList) </strong>which prints the contents of the BrowserList with one URL per line, placing *’s around the current URL. If we printed the final list in the example, we would have:</li>

  </ol></li>

</ul>

<strong> </strong>

<a href="https://www.google.com/">www.google.com</a> <a href="https://www.yahoo.com/">www.yahoo.com</a> *www.utsa.edu* 3) p3Input.txt.  This file contains a sample input file that you should process.  Each line will contain either BACK, FORWARD, PRINT, or a URL (don’t worry about checking the URL for errors).  If the line contains a URL, then you should call the goToURL() function to update the BrowserList.  If the line contains one of the other terms, then you should call the corresponding function.  The input file should be passed to the program like so: <strong>./p3 &lt; p3Input.txt </strong>

<ul>

 <li>c. Rename this file to your abc123.  This file is mostly empty right now.  It contains the main() function that you should complete.  In main, you should read a line from p3Input.txt (you can do this however you would like), detect if it is a URL or some other command, and update the BrowserList accordingly.</li>

 <li>Update the makefile to reflect your abc123.  Compile using <strong>make p3</strong>.</li>

</ul>







<strong>Submitting: </strong>

Please submit to the blackboard dropbox a zipped folder containing each of the files we have provided you along with the new DoublyLinkedList.c and BrowserList.c files that you create.





