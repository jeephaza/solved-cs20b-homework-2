Download Link: https://assignmentchef.com/product/solved-cs20b-homework-2
<br>
Explain why <em>false </em>is printed for this piece of code. How would you fix it to print <em>true</em>.

<table width="0">

 <tbody>

  <tr>

   <td width="434">String s1 = new String(“SMC”);String s2 = new String(“SMC”);System.out.println(s1 == s2);</td>

  </tr>

 </tbody>

</table>




<ol start="2">

 <li> True or False? Explain your answers.

  <ul>

   <li> You can define constructors for a Java interface.</li>

   <li> Classes implement interfaces.</li>

   <li>Classes extend interfaces.</li>

   <li> A class that implements an interface can include methods that are not required by the interface.</li>

   <li> A class that implements an interface can leave out methods that are required by an interface</li>

   <li> You can instantiate objects of an interface.</li>

  </ul></li>

</ol>

<h1>2           Programming exercises</h1>

For the programming exercises, please follow the provided instructions in the instructions.pdf. Each of the exercises below should be a separate zip of a Java project.

<ol>

 <li>Project 1: For this problem you must define a simple generic interface <em>PairInterface</em>, and two implementations of the interface, <em>BasicPair </em>and <em>ArrayPair</em>.</li>

</ol>

(a)Define a Java interface named <em>PairInterface</em>. A class that implements this interface allows creation of an object that holds a “pair” of objects of a specified type — these are referred to as the “first” object and the “second” object of the pair. We assume that classes implementing <em>PairInterface </em>provide constructors that accept

as arguments the values of the pair of objects. The <em>PairInterface </em>interface should require both setters and getters for the first and second objects. The actual type of the objects in the pair is specified when the <em>PairInterface </em>object is instantiated. Therefore, both the <em>PairInterface </em>interface and the classes that implement it should be generic. Suppose a class named <em>BasicPair </em>implements the <em>PairInterface </em>interface. A simple sample application that uses <em>BasicPair </em>is shown here. Its output would be ”apple orange.”

<table width="0">

 <tbody>

  <tr>

   <td width="404">public class Sample {public static void main (String[] args) { PairInterface myPair&lt;String&gt; = new BasicPair&lt;String&gt;(“apple”, “peach”); System.out.print(myPair.getFirst() + ” “); myPair.setSecond(“orange”);System.out.println(myPair.getSecond()); }}</td>

  </tr>

 </tbody>

</table>




<ul>

 <li> Create a class called <em>BasicPair </em>that implements the <em>PairInterface </em> This class should use two instance variables, <em>first </em>and <em>second</em>, to represent the two objects of the pair. Create a test driver application that demonstrates that the <em>BasicPair </em>class works correctly.</li>

 <li> Create a class called <em>ArrayPair </em>that implements the <em>PairInterface </em> This class should use an array of size 2 to represent the two objects of the pair. Create a test driver application that demonstrates that the <em>ArrayPair </em>class works correctly.</li>

</ul>

<ol start="2">

 <li>Project 2:  Add the following methods to the <strong>ArrayBoundedStack </strong>class, and create a test driver to show that they work correctly. In order to practice your array related coding skills, code each of these methods by accessing the internal variables of the ArrayBoundedStack, not by calling the previously defined public methods of the class.

  <ul>

   <li> String toString()—creates and returns a string that correctly represents the current stack. Such a method could prove useful for testing and debugging the class and for testing and debugging applications that use the class. Assume each stacked element already provided its own reasonable toString method.</li>

   <li> int size()—returns a count of how many items are currently on the stack. Do not add any instance variables to the ArrayBoundedStack class in order to implement this method.</li>

   <li> void popSome(int count)—removes the top count elements from the stack; throws StackUnderflowException if there are less than count elements on the stack.</li>

   <li> boolean swapStart()—if there are less than two elements on the stack returns false; otherwise it reverses the order of the top two elements on the</li>

  </ul></li>

</ol>

stack and returns true.

<strong>Please put and group all the methods you implement from above in the end of a single ArrayBoundedStack class so I can find it easily in your .java file</strong>.

<ol start="3">

 <li>Project 3:  Using the ArrayBoundedStack or ArrayListStack class, create an application <em>EditString </em>that prompts the user for a string and then repeatedly prompts the user for changes to the string, until the user enters an X, indicating the end of changes. Legal change operations are:</li>

</ol>

U—make all letters uppercase

L—make all letters lowercase

R—reverse the string

C ch1 ch2—change all occurrences of ch1 to ch2

Z—undo the most recent change

You may assume a “friendly user,” that is, the user will not enter anything illegal. When the user is finished the resultant string is printed. For example, if the user enters:

All dogs go to heaven

U R

Z

C O A

C A t

Z

the output from the program will be “ALL DAGS GA TA HEAVEN“

<strong>Make sure this driver test is possible to be compiled and run from command line. Include all the packages/dependencies in your submission!</strong>

<ol start="4">

 <li>Project 4: (20 points) Write code to <strong>detect </strong>if there are duplicates in a linked list stack or not. Make a test class that will test if the detection of the duplicates works. Test your code on the following stack of Strings: “top: A” → “B” → “B”→ “A”, for which your method should return <em>true</em>. Also write a test for which the method returns <em>false</em>. Make sure to document your code!</li>

</ol>

<strong>Bonus for the adventurous ones</strong>: write a code to <strong>remove </strong>the duplicates from the linked list stack. When fed with “top: A” → “B” → “B”→ “A”, it should update the linked list stack to contain only “top: A” → “B”.