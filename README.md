# SNOW-JavaScript-Arrays

-JavaScript arrays are used to store multiple values in a single variable.
```
var cars = ["Saab", "Volvo", "BMW"];
```
- An array is a special variable, which can hold more than one value at a time.
- If you have a list of items (a list of car names, for example), storing the cars in single variables could look like this:
```
var car1 = "Saab";
var car2 = "Volvo";
var car3 = "BMW";
```

## Creating an Array
- Using an array literal is the easiest way to create a JavaScript Array.
```
var cars = ["Saab", "Volvo", "BMW"];
```
 =Spaces and line breaks are not important. A declaration can span multiple lines
```
var cars = ["Saab","Volvo","BMW"];
Using the JavaScript Keyword new
var cars = new Array("Saab", "Volvo", "BMW");
```
## Accessing elements of an array
- You access an array element by referring to the index number.
 ```
var cars = ["Saab", "Volvo", "BMW"];document.getElementById("demo").innerHTML = cars[0];
```

## Changing an array element
```
var cars = ["Saab", "Volvo", "BMW"];
cars[0] = "Opel";
document.getElementById("demo").innerHTML = cars[0];
```
### Access the Full Array
- With JavaScript, the full array can be accessed by referring to the array name
```
var cars = ["Saab", "Volvo", "BMW"];
document.getElementById("demo").innerHTML = cars;
```
## Arrays are objects
- Arrays are a special type of objects. The typeof operator in JavaScript returns "object" for arrays.
- Arrays use numbers to access its "elements“
- In this example, person[0] returns John:
- ```
var person = ["John", "Doe", 46];
```
Objects use names to access its "members". 
In this example, person.firstName returns John:
```
var person = {firstName:"John", lastName:"Doe", age:46};
```
## Array Elements can be objects
Arrays are a special type of objects. The typeof operator in JavaScript returns "object" for arrays.
Arrays use numbers to access its "elements“
In this example, person[0] returns John:
var person = ["John", "Doe", 46];
Objects use names to access its "members". 
In this example, person.firstName returns John:
var person = {firstName:"John", lastName:"Doe", age:46};
![image](https://user-images.githubusercontent.com/12488769/148700108-5ff8d87c-c327-4a68-accc-63dd74efb1c8.png)

## Array Properties and methods
- The real strength of JavaScript arrays are the built-in array properties and methods

## The length property
The length property of an array returns the length of an array (the number of array elements).
Example
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];fruits.length;   // the length of fruits is 4
```

## Accessing the Array
- Accessing the First Array Element
fruits = ["Banana", "Orange", "Apple", "Mango"];var first = fruits[0];
- Accessing the Last Array Element
fruits = ["Banana", "Orange", "Apple", "Mango"];var last = fruits[fruits.length - 1];
- Looping Array Elements

![image](https://user-images.githubusercontent.com/12488769/148700213-a1244bdd-9b73-4743-a721-498424bb00b5.png)

## Adding array elements
The easiest way to add a new element to an array is using the push() method
var fruits = ["Banana", "Orange", "Apple", "Mango"];fruits.push("Lemon");    // adds a new element (Lemon) to fruits
New element can also be added to an array using the length property:
var fruits = ["Banana", "Orange", "Apple", "Mango"];fruits[fruits.length] = "Lemon";    // adds a new element (Lemon) to fruits


# JavaScript Array Methods
## COnverting Array to Strings
- The JavaScript method toString() converts an array to a string of (comma separated) array values.
```
Example
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
```
Result: Banana,Orange,Apple,Mango
The join() method also joins all array elements into a string.
It behaves just like toString(), but in addition you can specify the separator:
Example
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.join(" * ");
```
Result: Banana * Orange * Apple * Mango

## Pop
- The pop() method removes the last element from an array
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop();              // Removes the last element ("Mango") from fruits
```
The pop() method returns the value that was "popped out":
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var x = fruits.pop();      // the value of x is "Mango"
```
## Push
The push() method adds a new element to an array (at the end)
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi");       //  Adds a new element ("Kiwi") to fruits
```
The push() method returns the new array length:
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var x = fruits.push("Kiwi");   //  the value of x is 5
```
## shift elements
Shifting is equivalent to popping, working on the first element instead of the last.
The shift() method removes the first array element and "shifts" all other elements to a lower index.
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.shift();            // Removes the first element "Banana" from fruits
```
The shift() method returns the string that was "shifted out":
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var x = fruits.shift();    // the value of x is "Banana"
```
## unshift
- The unshift() method adds a new element to an array (at the beginning), and "unshifts" older elements:
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon");    // Adds a new element "Lemon" to fruits
```
The unshift() method returns the new array length.
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon");    // Returns 5
```
## Deleting elements
-Since JavaScript arrays are objects, elements can be deleted by using the JavaScript operator delete:
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
delete fruits[0];   // Changes the first element in fruits to undefined
```
## splice array
- The splice() method can be used to add new items to an array
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");
```
- The first parameter (2) defines the position where new elements should be added (spliced in).
- The second parameter (0) defines how many elements should be removed.
- The rest of the parameters ("Lemon" , "Kiwi") define the new elements to be added.

### Use splice to remove elements
- With clever parameter setting, you can use splice() to remove elements
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(0, 1);        // Removes the first element of fruits
```
- The first parameter (0) defines the position where new elements should be added (spliced in).
- The second parameter (1) defines how many elements should be removed.
- The rest of the parameters are omitted. No new elements will be added.

## Merge and concat arrays
The concat() method creates a new array 
by merging (concatenating) existing arrays
```
var myGirls = ["Cecilie", "Lone"];
var myBoys = ["Emil", "Tobias", "Linus"];
var myChildren = myGirls.concat(myBoys);   
// Concatenates (joins) myGirls and myBoys
The concat() method does not change the existing arrays. It always returns a new array.
var myChildren = arr1.concat(arr2, arr3);
var myChildren = arr1.concat("Peter"); 
```

## Slice an array
```
The slice() method slices out a piece of an array into a new array.
var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
var citrus = fruits.slice(1);
The slice() method creates a new array. 
It does not remove any elements from the source array.
The slice() method can take two arguments like slice(1, 3).
The method then selects elements from the start argument, and up to (but not including) the end argument.
var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
var citrus = fruits.slice(1, 3);
If the end argument is omitted, like in the first examples, the slice() method slices out the rest of the array
```
## Sort an array
The sort() method sorts an array alphabetically:
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();        // Sorts the elements of fruits
```

## Reverse an array
-mThe reverse() method reverses the elements in an array.
- You can use it to sort an array in descending order:
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();        // First sort the elements of fruits
fruits.reverse();     // Then reverse the order of the elements
```

## Numeric Sort
- By default, the sort() function sorts values as strings.
- This works well for strings ("Apple" comes before "Banana").
- However, if numbers are sorted as strings, "25" is bigger than "100", because "2" is bigger than "1".
- Because of this, the sort() method will produce incorrect result when sorting numbers.
-You can fix this by providing a compare function:
```
var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){
return a - b});
```












