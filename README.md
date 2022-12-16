Functions (hoisting)

function plantNeedsWater(day){
}

No. The above is hoisted as a declared function; the preceding is hoisted as a variable, which expression will be caught on the next pass.

When we assign using = in our code, the right hand side does not get hoisted. That is why we call them function expressions; they appear on the right hand side of an equals sign. On that side they are values.

They can also appear in arguments to other functions, in which case we refer to them as a callback. Essentially when the return value of one function given the inputs becomes the argument value of another function, per chance with additional arguments (that may include the initial inputs in some way).

Hoisting and binding are two different things to keep aware of in JS.

 > (function () {
     return foo();
     function foo(day="Wednesday"){
       return day==="Wednesday" ? "Water me!" : "Don't water me!";
     }
   })()
<- "Water me!"
 >
 > (function () {
     return foo(arguments[0]);
     function foo(day="Wednesday"){
       return day==="Wednesday" ? "Water me!" : "Don't water me!";
     }
   })('Thursday')
<- "Don't water me!"
 > 
The binding is to the return (response) value of the expression. That’s the key. Only foo was ever hoisted. Least not to mention is the arguments object which may or may not be populated. The first value may be of some interest…

This tells us that hoisting occurs within functions, not just at the global level. Whatever isn’t hoisted is treated as a value on the second pass. Recall that expressions are values, and utilize that going forward.


Functions : 

1)Fucntion Declarations :
function greet(){
console.log("hello jon");
}

2)Function Expressions :
const calculatedArea = function(width,height){
const area = width * height;
return area;
};

3)Arrow Functions 
const rectagleArea = (width,height) => {
let area = width * area ;
return area;
}

3.1)Concise Body Arrow Functions 
zero parameters
const function = () => {};

3.2)one parameter
const fucntionName = paramOne =>{};

3.3)two or more parameters
const functionName = (paramOne, paramTwo) =>{};

3.3.1)Single line block (no need of curly braces):
const sumNunmbers = number => number 1 + number2 ;

3.3.2)Multin - Lines Block
const sumNubers = number =>{
const sum = number + number;
return sum;
};


Arrays 

Array Literals 
const myArray = ['dog','cat','sport']

