# Type Script Question set25: 


1. What are the primitive types in TypeScript?
JavaScript has eight data types. Seven primitive types and one object Data type. The primitive types are number, string, boolean, bigint, symbol, undefined, and null. Everything else is an object in JavaScript.
The TypeScript Type System supports all of them and also brings its own special types. They are unknown, any, void & never.




2. Explain how the arrays work in TypeScript.
TypeScript supports arrays, similar to JavaScript. There are two ways to declare an array:
    1. Using square brackets. This method is similar to how you would declare arrays in JavaScript.
let fruits: string[] = ['Apple', 'Orange', 'Banana'];
    2. Using a generic array type, Array<elementType>.
let fruits: Array<string> = ['Apple', 'Orange', 'Banana']; 





3. What is any type, and when to use it?
The any type in TypeScript is a generic type used when a variable's type is unknown or when the variable's type hasn't yet been defined. 



4. What is void, and when to use the void type?
void represents the return value of functions which don't return a value. Whenever you see a function returning void , you are explicitly told there is no return value. All functions with no return value have an inferred return type of void . This should not be confused with a function returning undefined or null . 




5. What is an unknown type, and when to use it in TypeScript?
For type-safety
As it’s given in the introduction, an unknown type variable can only be assigned to another unknown type variable or a variable of type any. unknown type is displayed as “undefined”.
let a: unknown;
    console.log(a);
    let b: unknown = a;
    console.log(b);
    let c: any = a;
    console.log(c);

 let unknown: unknown;
    let num: number = unknown; // Error
    console.log(num);
error TS2322: Type 'unknown' is not assignable to type 'number'.
let num: number = a; // Error 





6. What are the different keywords to declare variables in TypeScript?
there are three different keywords to define variables: var , let , and const .
	Variable declared using let, const cannot be re-declared. 




7. Provide the syntax of a function with the type annotations.

Using the function keyword:
let add = function(a,b) { return a + b }


Using Arrow functions, It takes the form:
let add = (a,b) => { return a + b }


Functions defined in either of these ways can be called like any other function:
console.log(add(1,2)) // logs 3 

after adding type annotation to function expression
let add: (a: number, b: number) => number = (a,b) => { return a + b } 




8. How to create objects in TypeScript?
An object is an instance which contains set of key value pairs. The values can be scalar values or functions or even array of other objects. The syntax is given below −
Syntax
var object_name = { 
   key1: “value1”, //scalar value 
   key2: “value”,  
   key3: function() {
      //functions 
   }, 
   key4:[“content1”, “content2”] //collection  
}; 





9. How to specify optional properties in TypeScript?

type Foo = {
    bar?: number;
}

const a: Foo = {}; // This is now OK!

const b: Foo = { bar: 11 }; // This is still OK.

const c: Foo = { bar: undefined }; // This is also OK, somehow…? 




10. Explain the concept of null and its use in TypeScript.
the data type or value. 
The null is a keyword in TypeScript, which we can use to represent the absent or empty value. 
So, we can use 'null' to define the variable's data-type or initialize the variable 






11. What is undefined in TypeScript?
	Undefined is the default value for uninitialized variables 




12. Explain the purpose of the never type in TypeScript.
	
The never type represents the type of values that never occur. For instance, never is the return type for a function expression or an arrow function expression that always throws an exception or one that never returns. Variables also acquire the type never when narrowed by any type guards that can never be true.

// Function returning never must not have a reachable end point
function error(message: string): never {
  throw new Error(message);
}
 
// Inferred return type is never
function fail() {
  return error("Something failed");
}
 
// Function returning never must not have a reachable end point
function infiniteLoop(): never {
  while (true) {}
} 




13. Explain how enums work in TypeScript?
In TypeScript, enums, or enumerated types, are data structures of constant length that hold a set of constant values. 



14.
Explain the TypeScript class syntax.

class Student {  
    studCode: number;  
    studName: string;  
  
    constructor(code: number, name: string) {  
            this.studName = name;  
            this.studCode = code;  
    }  
 
   getGrade() : string {  
        return "A+" ;  
    }  
}  



15.
Explain the arrow function syntax in TypeScript.
