Credits : These are my notes from various JS Course : Javascript Mastery, Sheriyan coding school, Namaste JS : Akshay Saini

Socials : 
- [Hardikk kamboj Twitter](https://twitter.com/HdKamboj)
- [Hardikk Kamboj LinkedIn](https://www.linkedin.com/in/hardikk-kamboj/)
### Variables
- Let - can be changed -> braces scoped -> cannot be aaded to window object
- const - constants in js - cannot be changed 
- Var - can be changed ( with some scope constraints) -> scope is inside function -> adds itself to window object
- Valid First characters for naming -> $ or _
- Multiple same name vars cannot be there

#### Data Types
- String - sigle, double and backticks(``) qoutes. - Can use JS in it - ${ js inside here}
- Number - Number normal
- Null - null value ( can be assigned)
- Undefined - no defined value ( cannot be assigned )
- Typeof- to know the type of data type
- Object - group variables and store group of data types. ` const object1={ name :'John', age:25,}  with dot notation to access the property.`
- Array -> object 

### statically typed vs dynamically typed languages

js - dynamic - var can hold any data
c++ - statically typed

### Operations
-> `+,-,*,/`
-> modulo - %
-> exponent - `**
	-> comparison `< > ==(is equal)  ( true or false ),!=(not equal), === ( strict equals)`

Strict vs Loose equality  
```
== vs ===
5===5 -> true
5 == "5" -> true
5 === "5" -> false

=== -> compares both values and Data types
- true only when both are equal (Use it more )

== -> Doesnt compare data types
```

### Logical op
- AND && -> checks all and returns the last value ( truthy) if false is encountered ( return false value)
- OR || -> returns the first value (truthy) ( returns the first true) and if false then the last false value
- NOT -> ! -> reverse bool value

### TRUTHY VS FALSY
- 1, string, any other number, { }, [ ]- truthy 
- 0, null, false, ' ', Nan, Undefined -> falsy

### Switch Statements
```
switch(value){
case 'choice':
	console.log("stiuff")
	break;
default:
	cosole.log("default value")
}
```

Ternary Operator : 
```
if(){

}
else if{

}
else{

}

or 

? : notation 

condition ? True : false 


```
### Loops 
```
1. For loop - for(let i=0; i<something; i++)
2. While loop - While(condition){
	what to do 
} 
DRY PRINCIPAL -> DO Repeat Yourself
```

### Functions
```
// Function declaration - defining
// Function Call -> calling/executing the function

function testing(parameter){
	return parameter*parameter;
}

// call
const result = testing(argument to be passed)

result stores the value

// Annonomous function

const name = function(params){
// statements
}

// Arrow Functions

const name = (params) => {
	// statements
}

// Arrow with only one line

const name = (params) => params * params 


// Function with defualt value

const add = (a=0,b=0) => {
return a + b;
}

const result = add(2);
```

### Scope
- Where are the variables we make are available
- block, function and global scope

```
// Global scope 

const name = 'john'

const logName = () => {
	console.log(name);
}
logName();

// Local Scope / function scope

const hey = () => {
	// Local to this function
	const name = 'phil'
	console.log(name);
}

```

### Hoisting 
- JS mechanism where variable and function declarations are moved to the top of their scope before code execution.
```
console.log(age);

var age = 20; // only the declarations goes to the top not the value;

--> undefined -> hoisting

case 2.

var hoist
console.log(hoist);
hoist = "something"

--> undefined ( hoisting )

case 3 :
function hoist(){
console.log(message);
var message = 'test';
}
hoist();

--> undefined

if function call is done first
hoist();
function hoist(){
var message = 'test';
console.log(message);

}
--> Test
Hoisting was done with function is time

// For consts and let variable
console.log(age);
const age = 25

--> error (no hoisting in modern js for consts and let)


hoist();
const hoist = () => {
console.log(message)
}

--> error 
```

### Closures

![[Pasted image 20231129030115.png]]

- As soon as the function is done with the execution all of it's content is gone, and that's why we cannot access the local scope var outside the function.

- Function inside a function
![[Pasted image 20231129030524.png]]

--> Access to the var of the parent scope : due to the closures.
-> that's why we get both Hi and Hello above
-> The inner data is not getting deleted here.
![[Pasted image 20231129030911.png]]

### Strings 

- types ` ' ', " ", `` `
- property ` string.length, string[position], Cases : string.toLowerCase(), string.toUpperCase() -> store them in a new variable as well, String.indexOf('word') -> searchs the first substring, save it to a var as well, string.includes('word')-> true or false`
- Substing of a string - slice(start,end) 
- Split a string into single chars -split method 
	string.split('  ');  splits it on a each character, word. -> turns into an array
- Reverse - reverse method works on arrays ->
  
	  First we turn the string into an array using the split method and then use reverse method to reverse the characters.
	const reversed = string1.split("").reverse().join
- String.trim() -> removes the spaces : used for storing emails.

### Arrays 
- Ordered Collection of Data
- const array = ['ele1', 'el2'];
- loop over array -> for loop
-  Array methods - push, pop, shift(remove first element of array), unshift(adds new value to the start of the array)
-  Array Splice and Array Slice - 
	  Splice -> array.splice(where to add, how many to remove, what all to add) : adds or remove and
	  ![[Pasted image 20231130093217.png]]

	Slice -> array.slice(start,end) ->copy certains parts of an array into a newly created array.
	from ( start to end) excluding end.

- Array For Each : 
	- easier way to write for loop
	- Does not have a return value
```
		array.forEach(value, index) => {
		console.log(value,index)
	}
```

![[Pasted image 20231130093741.png]]![[Pasted image 20231130093934.png]]
![[Pasted image 20231130094022.png]]

- Array map method : 
	-  It allocates memory to store and return value ( opposite to the for each method)
	- Gives a new array all together
![[Pasted image 20231130094341.png]]

- Array Filter method :
	- It filters certain elements from an array. 
	- for ex- if you want only positive values
	- Doesnt change the old array
	- Returns a new array
	![[Pasted image 20231130094702.png]]

	- Real life ex - 
		![[Pasted image 20231130095055.png]]

-  Array Find  - returns the first value that satisfy the condition.
	![[Pasted image 20231130095426.png]]
	![[Pasted image 20231130095500.png]]

- Array includes - checks if array includes something or not -> returns a Boolean value.
	- It is case sensitive
	![[Pasted image 20231130095738.png]]

- Array Sort - sorts the array
	- Modifies the same array
	- array.sort()
	- Ascending/ decending value 
	![[Pasted image 20231130095954.png]]
	![[Pasted image 20231130100019.png]]
	
- Array Some and Array Every 
	- Array Some - are some elements ( checks a condition) and returns true or false.
	- ![[Pasted image 20231130100234.png]]
	- Array Every - Check if every element is passing some condition
	- ![[Pasted image 20231130100302.png]]

	- Array Reduce - iterates over all the values and computes them to a single value
		- No need of an external var is there
		- Same example with forEach and reduce method 
		- For each :
		 ![[Pasted image 20231130101017.png]]
		 - Reduce : 
		 - Takes in 2 arguments and a callback-function value called accumulator
		 - 0 is the initial value
		 ![[Pasted image 20231130101158.png]]
		 ![[Pasted image 20231130101405.png]]
### Objects

- Objects are unordered collection of related data
- In form of key-value pairs
```
const person = {
firstName:'john'
lastName: 'Doe'
age: '40'
car = {
	brand: 'maruti'
	year: 2016
	color: 'red'
}
}
```

- Object Methods 
	- another property of an obj that is a function
		![[Pasted image 20231130102903.png]]
		![[Pasted image 20231130103053.png]]
- Accessing - Adding and Updating object properties
	- Access - Use "DOT" notation
	- Add - use dot notation and { brackets } with key value pairs
		![[Pasted image 20231130103513.png]]
	
	- Access using [ Sqaure Brackets ]  - can access properties dynamically.
		![[Pasted image 20231130103607.png]]
		- Can access properties with dashes/ spaces using a string.
		 ![[Pasted image 20231130103733.png]]
- Built In Methods
	- object.keys() -> creates an array containing the keys of an object.
	 ![[Pasted image 20231130105858.png]]
	- Object.values() : values of the keys
	![[Pasted image 20231130105933.png]]

	- Object.entries() : creates a nested array of key/value pairs of an object.
	![[Pasted image 20231130110105.png]]
	- To display them all - ![[Pasted image 20231130110134.png]]
	- Object.freeze() : prevents modification to properties and values of an object.
		![[Pasted image 20231130110305.png]]

### Values Vs Reference - Deep and Shallow Clone

- The concept comes in  play when we are copying values
	
 - For numbers
		![[Pasted image 20231202091614.png]]
 
	- Complex values - ![[Pasted image 20231202091743.png]]
	   - Objects -
	   - ![[Pasted image 20231202091831.png]]
	   - why is it behaving like this in complex data types?
		   - when a variable is assigned a primitive value it just copies that value. ( number and string) ( copy by value )
		   - When a variable is assigned a non-primitive value ( array, objects, functions) -> it is given an address to the location in the memory of that variable. ( copied by reference -> location to memory )
		   - ![[Pasted image 20231202092156.png]]
		   - Even if the values are equal they point to the different location in memory.
		   - ![[Pasted image 20231202092231.png]]
		   - Now they hold the same location in memory.
	
 - Shallow Cloning : 
	 - Cloning arrays 
		 - Spread operator ( ... ) -> get values individually
			 ![[Pasted image 20231202092435.png]]
			 ![[Pasted image 20231202092535.png]]
			 -  In the second image 2 copies are created, first is equal as they point to same location in memory. 
			 - Newnumber array is not pointing to the same location, as they represent 2 different arrays.
			 - ![[Pasted image 20231202092741.png]]
			 - The Newly created array using the spread operator remains unchanged, meaning it is a shallow clone.
		 -  Array.slice ( ) ->  also creates a shallow clone -> creates a completely diffrent array pointing to a different location in memory.
			 -  ![[Pasted image 20231202093034.png]]
		- 
	- Cloning Objects : 
		- Spread operator ( ... )
			- ![[Pasted image 20231202093220.png]]
		- Object.assign({new object}, og object )
			- ![[Pasted image 20231202093301.png]]
- Deep Cloning :
	-  Issue with Shallow : 
		- ![[Pasted image 20231202093726.png]]
		- If the car color, which is an object inside an object has to be changed, the spread operator will just keep on increasing, as we have to mention the car obj as well in the spread operator for it to work, otherwise the car color will not change as the location we passed is only for the outer parent obj.
	-  Solution : This is for deeply nested obj we need a deep clone, for an obj to be a deep clone it needs to destroy all the references.
		- JSON.stringify( ) : Converts all the JS obj into string, thereby all the references are destroyed.
			- ![[Pasted image 20231202094325.png]]
		- JSON.parse( ) : to turn it back into a an obj we use parse()
			- ![[Pasted image 20231202094404.png]]
			  It is an obj but an obj that is the deep clone of the persons obj.
		- Shortcut 
			- ![[Pasted image 20231202094450.png]]
		- Result : deep cloning 
			- ![[Pasted image 20231202094557.png]]
### DOM : Document object model
- Accessing the elements in our html, via Javascript using certain methods : 
	- document.getElementById() - get the elements by the id name
	- document.getElementsByTagName( 'h1') - returns all the elements by that tag
	- document.getElementsByClassName( 'h1') - same but with classname
	- document.querySelectorAll('h2.classname') : returns all the h2 with classname "what ever the classname is"
		- can use # to target ids, . to target classnames or just Tagname to target any tagname.
- Element Properties -
		 ![[Pasted image 20231202100112.png]]
- Methods :
	- addEventListener
		- ![[Pasted image 20231202100320.png]]
	-  getBoundingClientRect( )
		- ![[Pasted image 20231202100411.png]]
	- hasAttribute( ) 
		- ![[Pasted image 20231202100447.png]]
### Classes in DOM :
	![[Pasted image 20231202101009.png]]
- Creating Nodes
		- document.createElement("h1")
			- appendChild( ) : to add it to the dom
			- InnerText : to add the text to that created element
			- InnerHtml : To add html to that element     
- Traversing :
	- ![[Pasted image 20231202101452.png]]
- Removing : 
	- ![[Pasted image 20231202101531.png]]

### New Keyword 
- Functionality : Creates a new empty object
- diffrences with normal way of creating it 
	- ![[Pasted image 20231202102247.png]]
	- For just normal creation it is not used that much.
-  Uses? 
	- Can use a lot of properties of present objs as everything in JS is an Obj.
		- ![[Pasted image 20231202102559.png]]
	- Dates
		- ![[Pasted image 20231202102405.png]]
		- This date methods are extended of a different object.

### This Keyword
- Used to reference the obj that is executing the current function.
- Every function has a reference to it, in it's current execution context.
- Cannot use in arrow function
	- ![[Pasted image 20231202102836.png]]
- This keywords points to a specific object 
	- Without any function : references to the window object
		- ![[Pasted image 20231202103002.png]]
	- Inside a function :  Refers to the Object 'this ' keyword in
		- ![[Pasted image 20231202103142.png]]
	- Example : 
		- ![[Pasted image 20231202103352.png]]
### Classes
- It is  SCHEMA for an obj that can save many values
- Constructor is just like parameters in a function ( keys are passed inside)
-  Initiating a user for that class
	![[Pasted image 20231202105001.png]]

- Using Normal Functions 
	- ![[Pasted image 20231202105146.png]]
### Intervals and Trimers 
- setInterval() -> 1000 is 1 second ( counted in miliseconds)
- clearInterval() -> clears the interval once it is done
	- ![[Pasted image 20231202105536.png]]
- setTimeout : -> wait certain amount of time before executing a chunk of code
- clearTimeout : -> 
		![[Pasted image 20231202105719.png]]
- Asynchronous Nature :
	- ![[Pasted image 20231202105901.png]]
### Asynchronous JavaScript
- Synchronous : code is executed Line by Line and tasks are completed instantly.
	- There is no Time delay in the completion of the tasks for those lines of code.
	- Example : ![[Pasted image 20231202110209.png]]
- Asynchronous : 
	- Using the same example showing Async code:
		- ![[Pasted image 20231202110340.png]]
	
	
- Here the code takes some time to run. These task are run in the background while tge js engine keeps executing other lines of code. When the result of the waiting gets available, it is then used in the program.
- This Happens because of something known as Event Loop.

### Callbacks 
- Data Fetching from API : Async : cannot be sure how long it will take
	- Sync : 
		  ![[Pasted image 20231203090912.png]]
	- Async : 
		-  ![[Pasted image 20231203091038.png]]
		- The error is there because the data was not returned from the function immediately, but after 2 secs.
		- To make it work we use Callback ( ) functions.
		- pass in a callback function which will run when the data is fetched
		-   After 2 secs we get
			- ![[Pasted image 20231203091402.png]]
		
### Callback HELL 
- A normal callback functionality looks like :
	- ![[Pasted image 20231203091601.png]]
	- We will replace callbacks with promises and async await due to the callback hell.
- A complicated functionality of callbacks - ex of social media app
	- ![[Pasted image 20231203091934.png]]
	- Now as the functionality grows it becomes a lot of code to do the same functionality that is called a CALLBACK HELL!!!
		- ![[Pasted image 20231203092147.png]]
		- This is not maintainable and also not DRY ( do not repeat yourself)
		- To solve this issue Promises were introduced.

### Promises
- They are objects that either return the successfully fetched data, or the error.
- It has two parameters resolve and reject
- Then keyword is used to invoke it, catch ( ) to get the error
	- Using the callback hell example
		 ![[Pasted image 20231203092558.png]]
		 ![[Pasted image 20231203092726.png]]
-  Multiple Promises
		 ![[Pasted image 20231203093009.png]]
	- The calling will be changed as :
		- ![[Pasted image 20231203093232.png]]
		 
### Async () Await ()
- It is an easier and a cleaner way to work with promises
- They look like sync functions so they are easier to write
- Async functions returns promises
	- ![[Pasted image 20231203093523.png]]
	- ![[Pasted image 20231203093537.png]]
- Await Keyword : Waits for the promises to return a result.
	- If you want you use await it needs to be inside an async function
	- This is good as we do not have to use then() or fetch()
		- ![[Pasted image 20231203093730.png]]
		- Using the callback hell example 
			- ![[Pasted image 20231203094012.png]]
### Import and Export
-  To export one thing from a file
	- `export default name`
- To Import  that thing from that  file 
	- `import name from 'path'`
- Add type = module in html src 
	-  ![[Pasted image 20231203094806.png]]
- Example 
	- ![[Pasted image 20231203094752.png]]
- To export and import multiple  things out of one file 
-  Add export keyword before all the things 
- In Import use { } and add names of things you want to import
	- ![[Pasted image 20231203095059.png]]
	- ![[Pasted image 20231203095044.png]]
- In import you can change the name of the import as well but it is not good practice
		-
		 ![[Pasted image 20231203095305.png]]

### Extras
- Object and array Destructuring
	- Before : An object with Multiple values has been created, this is DRY 
		- ![[Pasted image 20231203100309.png]]
	- After : Using Destructuring
		- ![[Pasted image 20231203100424.png]]
		- For internal properties
			- ![[Pasted image 20231203100445.png]]
			- ![[Pasted image 20231203100502.png]]
	- Real Usecases :
	- ![[Pasted image 20231203100652.png]]
	- Array 
	- Before
		- ![[Pasted image 20231203100729.png]]
	- After 
		- ![[Pasted image 20231203100816.png]]
- First Class Functions 
	- A concept which tells that you can use functions as values
		- ![[Pasted image 20231203102009.png]]
		- This prints hey in the console
- Arrays Under the hood
	- Arrays are also objects, stored in a key value pair format
		- ![[Pasted image 20231203102244.png]]
		- You can add -ve index in array as well, it will acted as a key
- Higher Order Functions 
	- Accepting a function in parameters or returns a functions, forEach is a higher order function.
		- ![[Pasted image 20231203104725.png]]
		- ![[Pasted image 20231203104759.png]]
- Constructor Functions  
	- Normal function where this is used and new keyword is used when it is called
		- ![[Pasted image 20231203105300.png]]
	- Used when elements to be used have similar properties.
		- ![[Pasted image 20231203105531.png]]
- IIFE : Immediately Invoked Function Expression
	- Used to make Private Variables
		- ![[Pasted image 20231203110636.png]]
		- a here is a private variable, not available in DOM
		-  How to access
			- ![[Pasted image 20231203110844.png]]
			- ![[Pasted image 20231203110941.png]]
- Prototype :
	- Create an obj, followed by  a dot operator
	- Every obj created get prototype property
	- It contains many helper properties to complete our tasks 
	- for ex - .length property 
- Prototype Inheritance : 
	- ![[Pasted image 20231204093554.png]]
	-  This is called Inheritance : properties of parents getting passed to children, this is also the case in JS.
	-  This is what is called prototypal inheritance in JS
	- Base properties can be inherited and extra properties can be added.
		- `.__proto__` is the way to inherit it 
			- ![[Pasted image 20231204094326.png]]
-  call apply bind
	- If you want to change where this points inside a function containing an object
		- CALL 
		  ![[Pasted image 20231204094906.png]]
		  ![[Pasted image 20231204095005.png]]
		- Apply : Array is passed instead of the direct parameter values
			- Usecase : To change the value to this 
			- ![[Pasted image 20231204095102.png]]
		- Bind : Bind will not run, but will give a function, can be stored in a var
			- ![[Pasted image 20231204095208.png]]
- Pure and Impure Functions :
	- Pure :
		- It always returns same output for same input.
		- It will never change/update the value of a global variable. 
			- ![[Pasted image 20231204095543.png]]
	- Impure is just the opposite of pure
		- ![[Pasted image 20231204095631.png]]
		- ![[Pasted image 20231204095653.png]]
- Concurrency and Parallelism :
	- Concurrency : When sync code is running on Main stack and the async code on the side stack together.
	- Parallelism : This Focuses on making the task run on different processors and on their cores.
- Throttling : Controlling the number of executions of a code : ex - Scrolling