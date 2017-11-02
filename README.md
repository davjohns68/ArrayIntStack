# ArrayIntStack

A. Create your own Stack Class, call it ArrayIntStack.java and write the standard four public Stack methods as listed below (this is the easy part of the assignment).  Use at least one private helper method, maybe to ensure capacity of the array.  All methods in your ArrayIntStack must have O(constant) run-time.  Your ArrayIntStack extends no other Classes from the Java API.  You must provide a default constructor.

1. boolean empty();  Tests if this stack is empty (watch spelling here, as I will)
2. int peek();  Looks at the object at the top of this stack without removing it from the stack.
3. int pop();  Removes the object at the top of this stack and returns that object as the value of this function.
4. int push(int item); Pushes an item onto the top of this stack, return what was pushed.

Additional methods, code, etc... will also need to be provided, so the client can use an iterator:

5. public class IntStackIterator {  // similar to what the BJP authors show, but without a remove() implemented
6. public IntStackIterator iterator() method so the client can browse through the data with .next() etc...  Start the iterator at the top of the stack!!!

Suggestion:  Look at ArrayIntList.javaPreview the documentView in a new window as a reference to start his Assignment, Notice how ArrayIntList.javaPreview the documentView in a new window is fundamentally the ArrayIntList4 from the Chapter 15 downloads, plus an internal Iterator as used by Practice-IT, plus many other constructors (...) and operators that you do not need to do for this Assignment.  Understand how ArrayIntList.javaPreview the documentView in a new window works, and this Assignment will start to look easy.

Iterate through your array from top (end) to bottom (index 0), so the top of the Stack is returned from the first .next().  This is backwards from the textbook ArrayIntListIterator example, but what I require for your Stack, as then you need to really understand what an iterator is doing, and Stacks are kind of backwards when compared to Lists, the first thing you see is the top. It only makes sense, so push and pop work on the top (end) of the array.

You must throw an "appropriate" Exception (e.g. EmptyStackException) for illegal peek, pop, etc... operations.  Regarding size, let's say this remains O(constant) while the Stack size is less than 20 elements, beyond that the push(int) would need to throw a Stack Overflow.

