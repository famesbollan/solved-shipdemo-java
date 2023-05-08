Download Link: https://assignmentchef.com/product/solved-shipdemo-java
<br>
This lab is meant to further your understanding of inheritance, polymorphism, and abstract classes. This lab should further help you (as did last week’s lab) to complete the first programming project.

I.   Inheritance – 55 points

This part of the lab is a more involved version of the inheritance programming part of last week’s lab. Since that time, you’ve learned about polymorphism, and abstract classes and methods, and you’ve been told that:

<strong>An abstract class cannot be instantiated explicitly. Only objects that are inherited from an abstract class can be instantiated.</strong>

For this part of the lab, you will write an abstract superclass, Ship, and two subclasses, CargoShip and CruiseShip. The class Ship is abstract, so you cannot directly instantiate an object of type Ship. The UML diagrams (note that inheritance (arrows) is NOT shown in this UML diagram):

<img decoding="async" alt="Ship -name String yearBuilt int numProellars: int +Ship(name : String, year: int) setter and getter methods not shown +taString0 String CargoShip tonnage :int isDoubleHull boolean tCargoShip(name : String, year : int, tonnage int, doubleHull : baolean) setter and getter methods, and remaining toString method, not shown CruiseShip passengers int numPets int + CuiseShip(name : String, year int. passengers : int, mPets int) setter and getter methods, and remaining toString method, not shown " data-recalc-dims="1" data-src="https://i0.wp.com/d2vlcm61l7u1fs.cloudfront.net/media%2F46d%2F46dcf022-5ae4-47b5-aeae-0194c4ee125d%2FphpItS4oA.png?w=980" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" src="https://i0.wp.com/d2vlcm61l7u1fs.cloudfront.net/media%2F46d%2F46dcf022-5ae4-47b5-aeae-0194c4ee125d%2FphpItS4oA.png?w=980" alt="Ship -name String yearBuilt int numProellars: int +Ship(name : String, year: int) setter and getter methods not shown +taString0 String CargoShip tonnage :int isDoubleHull boolean tCargoShip(name : String, year : int, tonnage int, doubleHull : baolean) setter and getter methods, and remaining toString method, not shown CruiseShip passengers int numPets int + CuiseShip(name : String, year int. passengers : int, mPets int) setter and getter methods, and remaining toString method, not shown " data-recalc-dims="1">

 </noscript>

To complete this part of the lab:

Write the Ship superclass, as described in the above top-most UML diagram. Several things to note:

The Ship class name is italicized, which means that the Ship class is abstract. You need to use the abstract java keyword, to indicate that the class is abstract

The toString() method in the Ship class, is italicized, so it is abstract. That means, that it cannot have a body, and that all subclasses of Ship MUST have an overriding toString method.

The class has a numPropellars field, but the constructor does NOT accept an argument that corresponds to the numPropellars field. You’ll need to decide how to set the value of numPropellars. There are multiple ways that you can do this (I am leaving this choice to you, and the UML diagram is intentionally vague in this regard).

Compile the Ship superclass as soon as you write it. Because it is not a child of any other class, you should be able to write code for it that is free of syntax errors, and it should compile.

Write the CargoShip subclass.

The Ship superclass does not have a default constructor, so in the CargoShip constructor, you’ll need to invoke the superclass constructor, using the super keyword, and pass to it the correct number of arguments (as specified in the Cargo class constructor).

You MUST write a toString method, whose argument list is identical to the argument list of the abstract method toString in the superclass. Notice that the subclass CargoShip does NOT have the field yearBuilt, so in the toString method, you’ll need to call the superclass’s getYearBuilt method, when you want to retrieve that information.

Compile the subclass. You can do this ONLY after the Ship superclass has been coded correctly, because the CargoShip class extends the Ship superclass.

Write the CruiseShip subclass.

The Ship superclass does not have a default constructor, so in the CruiseShip constructor, you’ll need to invoke the superclass constructor, using the super keyword, and passing into it the correct number of arguments (as specified in the Cargo class constructor).

You MUST write a toString method, whose argument list is identical to the argument list of the abstract method toString in the superclass. The same instructions apply to the toString method of this class, as for the CargoShip class.

Just as you did with the CargoShip subclass, compile this CruiseShip subclass.

II.   Ship Demo; Polymorphism – 45 Points

Recall that polymorphism, which means “many forms” refers to a superclass reference variable being able to reference objects of a subclass. For example, assume that the following superclass is defined:

public class Auto{ // content of class }

along with the following two subclasses

public class Convertible extends Auto{ // content of class}

public class Truck extends Auto{ // content of class}

Polymorphism, then, allows you to do the following:

Auto myAuto = new Truck();

Auto notMyAuto = new Convertible();

in which the reference variables myAuto and notMyAuto, both of type Auto, are referring to objects that are of type Truck and Convertible, respectively. This is allowed, because both Truck and Convertible are subclasses of Auto, so they both are specialized versions of an Auto.

For this part of the lab:

Create a file, <em>ShipDemo.java</em>

In the main method, create a final int variable, NUM_SHIPS, and assign it the value of at least 3.

Create an array, ships, that holds NUM_SHIPS of Ship references. Thus, you should have something like the following:

Ship[] ships = new Ship[NUM_SHIPS];

Populate the ships array, with objects of type CruiseShip and CargoShip. You’ll need to have as many lines of code to instantiate these objects as you have space in the array ships.

Write a for loop, that iterates over the array ships, and invokes the toString() method of each object.

Compile and debug your program. A sample invocation is shown in Figure 1.

<img decoding="async" alt="" data-recalc-dims="1" data-src="https://i0.wp.com/d2vlcm61l7u1fs.cloudfront.net/media%2F9f3%2F9f3a7a49-de39-486b-81a2-05f5ba52b3f2%2FphpYpdnUx.png?w=980" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" src="https://i0.wp.com/d2vlcm61l7u1fs.cloudfront.net/media%2F9f3%2F9f3a7a49-de39-486b-81a2-05f5ba52b3f2%2FphpYpdnUx.png?w=980" alt="" data-recalc-dims="1">

 </noscript>

III. Rubric and Submission

<table border="0" cellspacing="0" cellpadding="0">

 <tbody>

  <tr>

   <td>Item</td>

   <td>Points</td>

  </tr>

  <tr>

   <td><em>Ship.java</em> written correctly, and it compiles</td>

   <td>15</td>

  </tr>

  <tr>

   <td>Subclasses <em>CargoShip.java</em> and <em>CruiseShip.java</em> written correctly, and they compile</td>

   <td>40</td>

  </tr>

  <tr>

   <td><strong><em>ShipDemo.java</em> written, in which you have an array of at least three Ship objects, for each of which the toString method is invoked</strong></td>

   <td>45</td>

  </tr>

  <tr>

   <td>Total</td>

   <td>100</td>

  </tr>

 </tbody>

</table>

Zip your java files (Ship.java, CargoShip.java, CruiseShip.java, and ShipDemo.java) and submit the zip file via Canvas.