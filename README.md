Download Link: https://assignmentchef.com/product/solved-comp1210-project-7-dodecahedron-list2-with-junit-tests
<br>
<strong>Deliverables </strong>

Your project files should be submitted to Web-CAT by the due date and time specified.  Note that there is also an optional Skeleton Code assignment this week which will indicate level of coverage your tests have achieved (there is no late penalty since the skeleton code assignment is ungraded for this project).  The files you submit to skeleton code assignment may be incomplete in the sense that method bodies have at least a return statement if applicable or they may be essentially completed files.  In order to avoid a late penalty for the project, you must submit your <u>completed code</u> files to Web-CAT no later than 11:59 PM on the due date for the completed code.  You may submit your <u>completed code</u> up to 24 hours after the due date, but there is a late penalty of 15 points.  No projects will be accepted after the one-day late period.  If you are unable to submit via Web-CAT, you should e-mail your project Java files in a zip file to your TA before the deadline. The grade for the <strong>Part A Completed Code</strong> submission (Dodecahedron.java, DodecahedronTest.java, DodecahedronList2.java, and DodecahedronList2Test.java) will be determined by the tests that you pass or fail in your test files and by the level of coverage attained in your source files.  The <strong>Part B Completed Code</strong> will be tested against the test methods in your test files as well as usual correctness tests in Web-CAT.  The 7B Completed Code assignment will <u>not</u> be posted until after 7A Completed Code assignment is closed (i.e., after the late submission day).




<strong>Files to submit to Web-CAT</strong> (all three files must be submitted together):<strong>   </strong>

<ul>

 <li>java, DodecahedronTest.java</li>

 <li>java, DodecahedronList2Test.java</li>

</ul>




<strong>Specifications – </strong><strong>Use arrays in this project; ArrayLists are not allowed!</strong><strong>   </strong>

<strong>Overview</strong>:  This project consists of four classes: (1) Dodecahedron is a class representing a Dodecahedron object; (2) DodecahedronTest class is a JUnit test class which contains one or more test methods for each method in the Dodecahedron class; (3) DodecahedronList2 is a class representing a Dodecahedron list object; and (4) DodecahedronList2Test class is a JUnit test class which contains one or more test methods for each method in the DodecahedronList2 class.  <u> Note that</u> <u>there is no requirement for a class with a main method in this project</u>.




<strong><u>Since you will be modifying classes from the previous project, I strongly recommend that you</u> <u>create a new folder for this project with a copy of your Dodecahedron class and</u> <u>DodecahedronList2 class from the previous project</u>.    </strong>

<strong> </strong>

<strong><u>You should create a jGRASP project and add your Dodecahedron class and</u> </strong>

<strong><u>DodecahedronList2 class.  With this project is open, your test files will be automatically added</u> <u>to the project when they are created.  You will be able to run all test files by clicking the JUnit</u> <u>run button on the Open Projects toolbar</u>. </strong>

<em> </em>

<em>New requirements and design specifications are underlined in the descriptions below to help you identify them</em>.




<ul>

 <li><strong>Dodecahedron.java </strong>(a modification of the <strong>Dodecahedron </strong>class in the previous project; <u>new</u> <u>requirements are underlined below</u>)</li>

</ul>

<strong> </strong>

<strong>Requirements</strong>: Create a Dodecahedron class that stores the label, color, and edge (i.e., length of an edge, which must be greater than zero).  The Dodecahedron class also includes methods to set and get each of these fields, as well as methods to calculate the surface area, volume, and surface

to volume ratio of a Dodecahedron object, and a method to provide a String value of a Dodecahedron object (i.e., a class instance).




<table width="586">

 <tbody>

  <tr>

   <td colspan="3" width="586">A dodecahedron has 12 equal pentagonal faces, 20 vertices, and 30 edges as depicted below. The formulas are provided to assist you in computing return values for the respective Dodecahedron methods described in this project.</td>

  </tr>

  <tr>

   <td width="198"> </td>

   <td width="184"> Surface Area (A) Volume (V) Edge length (a) Surface/Volume ratio (A/V)</td>

   <td width="204">    </td>

  </tr>

  <tr>

   <td colspan="3" width="586"> </td>

  </tr>

 </tbody>

</table>

<strong>       </strong>

<strong>Design</strong>:  The Dodecahedron class has fields, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields:</strong> Instance Variables – label of type String, color of type String, and edge of type double. Initialize the Strings to “” and the double to 0 in their respective declarations. These instance variables should be private so that they are not directly accessible from outside of the Dodecahedron class, and these should be the only instance variables in the class.</li>

</ul>

<u>Class Variable – count of type int should be private and static, and it should be initialized to</u> <u>zero</u>.




<ul>

 <li><strong>Constructor</strong>: Your Dodecahedron class must contain a public constructor that accepts three parameters (see types of above) representing the label, color, and edge. Instead of assigning the parameters directly to the fields, the respective set method for each field (described below) should be called. For example, instead of the statement label = labelIn; use the statement setLabel(labelIn);</li>

</ul>




<u>The constructor should increment the class variable count each time a Dodecahedron is</u> <u>constructed</u>.




Below are examples of how the constructor could be used to create Dodecahedron objects.  Note that although String and numeric literals are used for the actual parameters (or arguments) in these examples, variables of the required type could have been used instead of the literals.




Dodecahedron example1 = new Dodecahedron(“Small Example”, “blue”, 0.25);




Dodecahedron example2 = new Dodecahedron(” Medium Example “, “orange”, 10.1);




Dodecahedron example3 = new Dodecahedron(“Large Example”, “silver  “, 200.5);




<ul>

 <li><strong>Methods</strong>: Usually a class provides methods to access and modify each of its instance variables (known as get and set methods) along with any other required methods. The methods for Dodecahedron, which should each be public, are described below.  See formulas in Code and Test below. o getLabel:  Accepts no parameters and returns a String representing the label field.

  <ul>

   <li>setLabel: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the label field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

   <li>getColor: Accepts no parameters and returns a String representing the color field.</li>

   <li>setColor: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the color field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

   <li>getEdge: Accepts no parameters and returns a double representing the edge field.</li>

   <li>setEdge: Accepts a double parameter and returns a boolean as follows. If the edge is greater than zero, sets the edge field to the double passed in and returns true.  Otherwise, the method returns false and the edge is not set.  o surfaceArea:  Accepts no parameters and returns the double value for the total surface area calculated using the value for edge.</li>

   <li>volume: Accepts no parameters and returns the double value for the volume calculated using the value for edge.</li>

   <li>surfaceToVolumeRatio: Accepts no parameters and returns the double value calculated by dividing the total surface area by the volume.</li>

   <li>toString: Returns a String (does<u> not </u>begin with 
) containing the information about the Dodecahedron object formatted as shown below, including decimal formatting (“#,##0.0##”) for the double values.  Newline and tab escape sequences should be used to achieve the proper layout.  In addition to the field values (or corresponding “get” methods), the following methods should be used to compute appropriate values in the toString method: surfaceArea(), volume(), and surfaceToVolumeRatio().  Each line should have no trailing spaces (e.g., there should be no spaces before a newline (
) character).  The toString value for example1, example2, and example3 respectively are shown below (the blank lines are not part of the toString values).</li>

  </ul></li>

</ul>




Dodecahedron “Small Example” is “blue” with 30 edges of length 0.25 units.    surface area = 1.29 square units    volume = 0.12 cubic units    surface/volume ratio = 10.777




Dodecahedron “Medium Example” is “orange” with 30 edges of length 10.1 units.    surface area = 2,106.071 square units    volume = 7,895.319 cubic units    surface/volume ratio = 0.267




Dodecahedron “Large Example” is “silver” with 30 edges of length 200.5 units.    surface area = 829,963.459 square units    volume = 61,765,889.248 cubic units    surface/volume ratio = 0.013




<strong> </strong>

<ul>

 <li><u>getCount: A static method that accepts no parameters and returns an int representing</u> <u>the static count field</u>.   o <u>resetCount:  A static method that returns nothing, accepts no parameters, and sets the</u> <u>static count field to zero</u>.</li>

 <li><u>equals: An instance method that accepts a parameter of type Object and returns false if</u> <u>the Object is a not a Dodecahedron; otherwise, when cast to a Dodecahedron, if it has the</u> <u>same field values as the Dodecahedron upon which the method was called. Otherwise, it</u> <u>returns false</u>. Note that this equals method with parameter type Object will be called by the JUnit Assert.assertEquals method when two Dodecahedron objects are checked for equality.</li>

</ul>




Below is a version you are free to use.

public boolean equals(Object obj) {




if (!(obj instanceof Dodecahedron)) {          return false;

}       else {

Dodecahedron d = (Dodecahedron) obj;

return (label.equalsIgnoreCase(d.getLabel())                             &amp;&amp; color.equalsIgnoreCase(d.getColor())

&amp;&amp; Math.abs(edge – d.getEdge()) &lt; .000001);

}

}

o <u>hashCode(): Accepts no parameters and returns zero of type int.  This method is</u> <u>required by Checkstyle if the </u><u>equals method above is implemented.</u>




<strong>Code and Test</strong>: As you implement the methods in your Dodecahedron class, you should compile it and then create test methods as described below for the DodecahedronTest class.




<ul>

 <li><strong>DodecahedronTest<u>.java</u> </strong></li>

</ul>




<strong>Requirements</strong>: <u>Create a DodecahedronTest class that contains a set of <em>test</em> methods to test each</u> <u>of the methods in Dodecahedron.</u>




<strong>Design</strong>: <u>Typically, in each test method, you will need to create an instance of Dodecahedron, call</u> <u>the method you are testing, and then make an assertion about the expected result and the actual</u> <u>result (note that the actual result is commonly the result of invoking the method unless it has a</u> <u>void return type).  You can think of a test method as simply formalizing or codifying what you</u> <u>have been doing in interactions to make sure a method is working correctly.  That is, the sequence</u> <u>of statements that you would enter in interactions to test a method should be entered into a single</u> <u>test method.  You should have at least one test method for each method in Dodecahedron, except</u> <u>for associated getters and setters which can be tested in the same method.  However, if a method</u> <u>contains conditional statements (e.g., an <em>if</em> statement) that results in more than one distinct</u> <u>outcome, you need a test method for each outcome.  For example, if the method returns boolean,</u> <u>you should have one test method where the expected return value is false and another test method</u> <u>that expects the return value to be true (also, each condition in boolean expression must be</u> <u>exercised true and false).  Collectively, these test methods are a set of test cases that can be</u> <u>invoked with a single click to test all of the methods in your Dodecahedron class</u>.

<strong> </strong>

<strong>Code and Test</strong>: <u>Since this is the first project requiring you to write JUnit test methods, a good</u> <u>strategy would be to begin by writing test methods for those methods in Dodecahedron that you</u> <u>“know” are correct.  By doing this, you will be able to concentrate on the getting the test methods</u> <u>correct.  That is, if the test method <em>fails</em>, it is most likely due to a defect in the test method itself</u> <u>rather the Dodecahedron method being testing.  As you become more familiar with the process of</u> <u>writing test methods, you will be better prepared to write the test methods for the new methods in</u> <u>Dodecahedron.  Be sure to call the Dodecahedron toString method in one of your test cases so</u> <u>that Web-CAT will consider the toString method to be “covered” in its coverage analysis.</u>  <u>Remember that you can set a breakpoint in a JUnit test method and run the test file in Debug</u> <u>mode.  Then, when you have an instance in the Debug tab, you can unfold it to see its values or</u> <u>you can open a canvas window and drag items from the Debug tab onto the canvas</u>.




<ul>

 <li><strong>java </strong>(a modification of the <strong>DodecahedronList2 </strong>class in the previous project; <u>new requirements are underlined below</u>)</li>

</ul>




<strong>Requirements</strong>: Create a DodecahedronList2 class that stores the name of the list and an array of

Dodecahedron objects.  It also includes methods that return the name of the list, number of Dodecahedron objects in the DodecahedronList2, total surface area, total volume, average surface area, average volume, and average surface to volume ratio for all Dodecahedron objects in the DodecahedronList2.  The toString method returns a String containing the name of the list followed by each Dodecahedron in the array, and a summaryInfo method returns summary information about the list (see below).




<strong>Design</strong>:  The DodecahedronList2 class has <u>three fields</u>, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (or instance variables): (1) a String representing the name of the list, (2) an array of Dodecahedron objects, and (3) an int representing the number of elements in the array of Dodecahedron objects. These are the only fields (or instance variables) that this class should have.</li>

 <li><strong>Constructor</strong>: Your DodecahedronList2 class must contain a constructor that accepts a parameter of type String representing the name of the list, a parameter of type</li>

</ul>

Dodecahedron[], representing the list of Dodecahedron objects, and a parameter of type int representing the number of elements in the Dodecahedron array.  These parameters should be used to assign the fields described above (i.e., the instance variables).

<strong> </strong>

<ul>

 <li><strong>Methods</strong>: The methods for DodecahedronList2 are described below. o getName: Returns a String representing the name of the list.</li>

</ul>

<ul>

 <li>numberOfDodecahedrons: Returns an int representing the number of</li>

</ul>

Dodecahedron objects in the DodecahedronList2.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong>

<ul>

 <li>totalSurfaceArea: Returns a double representing the total surface areas for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>totalVolume: Returns a double representing the total volumes for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>averageSurfaceArea: Returns a double representing the average surface area for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>averageVolume: Returns a double representing the average volume for all</li>

</ul>

Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong>

<ul>

 <li>averageSurfaceToVolumeRatio: Returns a double representing the average surface to volume ratio for all Dodecahedron objects in the list.  If there are zero Dodecahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>toString: Returns a String (does <u>not</u> begin with 
) containing the name of the list followed by each Dodecahedron in the list.  In the process of creating the return result, this toString() method should include a while loop that calls the toString() method for each Dodecahedron object in the list (adding a 
 before and after each).  Be sure to include appropriate newline escape sequences.  For an example, see <u>lines 2 through 19</u> in the output below from DodecahedronList2App for the <em>txt</em> input file. [Note that the toString result should <strong>not</strong> include the return value of summaryInfo().]</li>

 <li>summaryInfo: Returns a String (does<u> not </u>begin with 
) containing the name of the list (which can change depending of the value read from the file) followed by various summary items:  number of Dodecahedrons, total surface area, total volume, average surface area, average volume, and average surface to volume ratio.  Use “#,##0.0##” as the pattern to format the double values.</li>

 <li>getList: Returns the array of Dodecahedron objects (the second field above).</li>

 <li>readFile: Takes a String parameter representing the file name, reads in the file, storing the list name and creating an array of Dodecahedron objects, uses the list name, the array, and number of Dodecahedron objects in the array to create a</li>

</ul>

DodecahedronList2 object, and then returns the DodecahedronList2 object.  See note #1 under <u>Important Considerations</u> for the DodecahedronList2MenuApp class (last page) to see how this method should be called. <strong> </strong>

<ul>

 <li>addDodecahedron: Returns nothing but takes three parameters (label, color, and edge), creates a new Dodecahedron object, and adds it to the DodecahedronList2 object.</li>

 <li>findDodecahedron: Takes a label of a Dodecahedron as the String parameter and returns the corresponding Dodecahedron object if found in the DodecahedronList2</li>

</ul>

object; otherwise returns null.  Case should be ignored when attempting to match the label.

<ul>

 <li>deleteDodecahedron: Takes a String as a parameter that represents the label of the Dodecahedron and returns the Dodecahedron if it is found in the DodecahedronList2 object and deleted; otherwise returns null.  Case should be ignored when attempting to match the label; consider calling/using findDodecahedron in this method.  When an element is deleted from an array, elements to the right of the deleted element must be shifted to the left. After shifting the items to the left, the last Dodecahedron element in the array should be set to null.  Finally, the number of elements field must be decremented.</li>

 <li>editDodecahedron: Takes three parameters (label, color, and edge), uses the label to find the corresponding the Dodecahedron object in the list.  If found, sets the color and edge to the values passed in as parameters, and returns true.  If not found, returns false.</li>

</ul>

<strong> </strong>

<u>New method for Project 7</u>

<ul>

 <li><u>find</u>Dodecahedron<u>WithShortestEdge</u><u>: Returns the Dodecahedron with the</u> <u>shortest edge; if the list contains no Dodecahedron objects, returns null</u>.</li>

 <li><u>find</u>Dodecahedron<u>WithLongestEdge</u><u>: Returns the Dodecahedron with the</u> <u>longest edge; if the list contains no Dodecahedron objects, returns null</u>.</li>

 <li><u>find</u>Dodecahedron<u>WithSmallestVolume</u><u>: Returns the Dodecahedron with the</u> <u>smallest volume; if the list contains no Dodecahedron objects, returns null</u>.</li>

 <li><u>find</u>Dodecahedron<u>WithLargestVolume</u><u>: Returns the Dodecahedron with the</u> <u>largest volume; if the list contains no Dodecahedron objects, returns null</u>.</li>

</ul>

<strong> </strong>

<strong>Code and Test</strong>: Remember to import java.util.Scanner, java.io.File, java.io.IOException.  These classes will be needed in the readFile method which will require a throws clause for IOException.

Some of the methods above require that you use a loop to go through the objects in the array.  You may want to implement the class below in parallel with this one to facilitate testing.  That is, after implementing one to the methods above, you can implement the corresponding “case” in the switch for menu described below in the DodecahedronList2MenuApp class.




<ul>

 <li><strong><u>DodecahedronList2Test.java</u> </strong></li>

</ul>




<strong>Requirements</strong>: <u>Create a DodecahedronList2Test class that contains a set of <em>test</em> methods to test</u> <u>each of the methods in DodecahedronList2.</u>




<strong>Design</strong>: <u>Typically, in each test method, you will need to create an instance of</u>

<u>DodecahedronList2, call the method you are testing, and then make an assertion about the</u> <u>expected result and the actual result (note that the actual result is usually the result of invoking</u> <u>the method unless it has a void return type) .  You can think of a test method as simply</u> <u>formalizing or codifying what you have been doing in interactions to make sure a method is</u> <u>working correctly.  That is, the sequence of statements that you would enter in interactions to test</u> <u>a method should be entered into a single test method.  You should have at least one test method</u> <u>for each method in DodecahedronList2.  However, if a method contains conditional statements</u> <u>(e.g., an <em>if</em> statement) that results in more than one distinct outcome, you need a test method for</u> <u>each outcome.  For example, if the method returns boolean, you should have one test method</u> <u>where the expected return value is false and another test method that expects the return value to</u> <u>be true.  Collectively, these test methods are a set of test cases that can be invoked with a single</u> <u>click to test all of the methods in your DodecahedronList2 class</u>.

<strong> </strong>

<strong>Code and Test</strong>: <u>Since this is the first project requiring you to write JUnit test methods, a good</u> <u>strategy would be to begin by writing test methods for those methods in DodecahedronList2 that</u> <u>you “know” are correct.  By doing this, you will be able to concentrate on the getting the test</u> <u>methods correct.  That is, if the test method <em>fails</em>, it is most likely due to a defect in the test</u> <u>method itself rather the DodecahedronList2 method being testing.  As you become more familiar</u> <u>with the process of writing test methods, you will be better prepared to write the test methods for</u> <u>the new methods in DodecahedronList2.  Be sure to call the DodecahedronList2 toString method</u> <u>in one of your test cases so that Web-CAT will consider the toString method to be “covered” in</u> <u>its coverage analysis.  Remember that you can set a breakpoint in a JUnit test method and run the</u> <u>test file in Debug mode.  Then, when you have an instance in the Debug tab, you can unfold it to</u> <u>see its values or you can open a canvas window and drag items from the Debug tab onto the</u> <u>canvas</u>.




<u>When comparing two arrays for equality in JUnit, be sure to use Assert.assertArrayEquals rather</u> <u>than Assert.assertEquals</u>.  Assert.assertArrayEquals will return true only if the two arrays are the same length and the elements are equal based on an element by element comparison using the appropriate equals method.




<strong><u>Web-CAT</u> </strong>

<strong> </strong>

<u>Dodecahedron.java, DodecahedronTest.java, DodecahedronList2.java, and DodecahedronList2Test.java</u> <u>must be submitted to the <strong>Part A </strong>and<strong> Part B </strong>Web-CAT assignments</u>. Note that data files dodecahedron_data_1.txt and dodecahedron_data_0.txt are available in Web-CAT for you to use in your test methods. If you want to use your own data files, they should have a .txt extension, and they should be included with submission to Web-CAT (i.e., just add the .txt data file to your jGRASP project in the Source Files category).

<strong> </strong>

<strong><u>Assignment Part A – </u></strong><u>Web-CAT will use the results of your test methods and their level of coverage to</u> <u>determine your grade.  No reference correctness tests will be included in Web-CAT for assignment Part</u> <u>A; the reference correctness tests are simply the JUnit test methods that we use to grade your program (as</u> <u>we have done on previous projects).  When you submit to <strong>Part A, </strong>Web-CAT will provide feedback on</u> <u>failures (if any) of your test methods as well as how well your test methods covered the methods in your</u> <u>source files. You may need to add test methods to your test files in order to increase your grade.</u>




<strong><u>Assignment Part B – </u></strong><u>As with previous projects, <strong>Part B</strong> will include the reference correctness tests which</u> <u>we use to test all of your methods.  Web-CAT will use the results of these correctness tests as well as the</u> <u>results from your test classes to determine your project grade.  If you have written good test methods in</u> <u>your test files and your source classes pass all of them, then they should also pass our reference</u> <u>correctness tests</u>.