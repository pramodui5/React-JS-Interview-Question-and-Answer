# React-JS-Interview-Question-and-Answer
#### 1. What is Refs?
Refs provide a way to access DOM nodes or React elements created in the render method.
#### 2.	What is Promise used for? 
Promises are used to handle asynchronous operations in JavaScript. They are easy to manage when dealing with multiple asynchronous operations where callbacks can create callback hell leading to unmanageable code
#### 3.	Different phases of component life cycle
Each component in React has a lifecycle which you can monitor and manipulate during its three main phases. The three phases are: Mounting, Updating, and Unmounting.
#### 4.	Life cycle method
#### 5.	Error boundary 
Error boundaries are React components that catch JavaScript errors anywhere in their child component tree, log those errors, and display a fallback UI instead of the component tree that crashed.
#### 6.	HOC 
A higher-order component (HOC) is an advanced technique in React for reusing component logic. A higher-order component is a function that takes a component and returns a new component.
#### 7.	Lazy loading 
lazy() is a function that enables you to render a dynamic import as a regular component. Dynamic imports are a way of code-splitting, which is central to lazy loading. A core feature as of React 16.6, React. lazy() eliminates the need to use a third-party library such as react-loadable
 
#### 8.	Let var const 
**Var** - Scope:  The scope of the var keyword is the global or function scope. It means variables defined outside the function can be accessed globally, and variables defined inside a particular function can be accessed within the function. 

**let** keyword in JavaScript: The let keyword is an improved version of the var keyword. 
Scope: block scoped: The scope of a let variable is only block scoped. It can’t be accessible outside the particular block ({block}).

**const** keyword in JavaScript: The const keyword has all the properties that are the same as the let keyword, except the user cannot update it.
Scope: block scoped: When users declare a const variable, they need to initialize it, otherwise, it returns an error. The user cannot update the const variable once it is declared. 

Users cannot change the properties of the const object, but they can change the value of properties of the const object.
 
![image](https://user-images.githubusercontent.com/12524071/160590049-5a631922-5800-4076-87e0-dd2ef94e2a59.png)

#### 9.	What is Redux?
Redux is used mostly for **application state management**. Redux maintains the state of an entire application in a single immutable state tree (object), which can't be changed directly. When something changes, a new object is created (using actions and reducers).

An action is dispatched when a user interacts with the application. The root reducer function is called with the current state and the dispatched action.

#### 10.	Middleware(redux-thunk,redux-saga)
Redux middleware provides **a third-party extension point between dispatching an action, and the moment it reaches the reducer**. People use Redux middleware for logging, crash reporting, talking to an asynchronous API, routing, and more.

**Redux Thunk** is a middleware that **lets you call action creators that return a function instead of an action object**. That function receives the store's dispatch method, which is then used to dispatch regular synchronous actions inside the function's body once the asynchronous operations have been completed.

**Saga** works like a **separate thread or a background process** that is solely responsible for making your side effects or API calls unlike redux-thunk, which uses callbacks which may lead to situations like 'callback hell' in some cases. However, with the async/await system, this problem can be minimized in redux-thunk.

#### 11.	Generator function
The generator function **can return (or yield) the control back to the caller at any point**. Unlike the regular function, the generator can return (or yield) the multiple values, one after another, on the requirement.

A generator allows you to pause the execution of a function and resume it later. Generators are **useful when dealing with iterators and can simplify the asynchronous nature of Javascript**.

#### 12.	Unit test and its question 
#### 13.	Setstate and without setstate can update   
#### 14.	Application folder structure  - 
 
#### 15.	What is Usememo?
React has a built-in hook called **useMemo** that allows you to memoize expensive functions so that you can avoid calling them on every render. You simple pass in a function and an array of inputs and useMemo will only recompute the memoized value when one of the inputs has changed.

UseMemo is one of the hooks offered by React. This hook allows developers to cache the value of a variable along with a dependency list. ... Once the component re-renders, it will fetch the value from the cache instead of having to loop through an array or process data again and again.

import { useMemo } from 'react';
function MyComponent({ prop }) {
const callback = () => {
return 'Result';
const memoizedCallback = useMemo(() => callback, [prop]);
return <ChildComponent callback={memoizedCallback} />;

#### 16.	Usecall back  
The **useCallback** hook is used when you have a component in which the child is rerendering again and again without need. Pass an inline callback and an array of dependencies. useCallback will return a memoized version of the callback that only changes if one of the dependencies has changed.

#### 17. What is the difference between useMemo and useCallback?
**UseCallback** is used to optimize the rendering behavior of your React function components, while **useMemo** is used to memoize expensive functions to avoid having to call them on every render.

#### 18.	Usereducer 
The useReducer is a hook I use sometimes to manage the state of the application. It is very similar to the useState hook, just more complex. It acts as an alternate hook to the useState hook to manage complex state in your application. The useReducer hook uses the same concept as the reducers in Redux.

#### 19.	useContext 
“useContext” hook is used to create common data that can be accessed throughout the component hierarchy without passing the props down manually to each level. Context defined will be available to all the child components without involving “props”

#### 20.	Spread operator 
The spread operator is a new addition to the set of operators in JavaScript ES6. It takes in an iterable (e.g an array) and expands it into individual elements. The spread operator is commonly used to make shallow copies of JS objects. Using this operator makes the code concise and enhances its readability.
Object spread operator can be used to clone an object or merge objects into one. ... When merging objects, the spread operator defines new properties while the Object.

#### 21.	Rest  operator 
The rest operator (…) allows us to call a function with any number of arguments and then access those excess arguments as an array. The rest operator also allows us in destructuring array or objects.

#### 22.	Deep copy and shallow copy 
A deep copying means that value of the new variable is disconnected from the original variable while a shallow copy means that some values are still connected to the original variable.

**Shallow Copy**: When a reference variable is copied into a new reference variable using the assignment operator, a shallow copy of the referenced object is created. In simple words, a reference variable mainly stores the address of the object it refers to. When a new reference variable is assigned the value of the old reference variable, the address stored in the old reference variable is copied into the new one. This means both the old and new reference variable point to the same object in memory. As a result if the state of the object changes through any of the reference variables it is reflected for both. Let us take an example to understand it better.

**Deep Copy**: Unlike the shallow copy, deep copy makes a copy of all the members of the old object, allocates separate memory location for the new object and then assigns the copied members to the new object. In this way, both the objects are independent of each other and in case of any modification to either one the other is not affected. Also, if one of the objects is deleted the other still remains in the memory. Now to create a deep copy of an object in JavaScript we use JSON.parse() and JSON.stringify() methods.

#### 23.	Forwarding ref 
Ref forwarding is a technique for automatically passing a ref through a component to one of its children. This is typically not necessary for most components in the application. However, it can be useful for some kinds of components, especially in reusable component libraries.

We need a way to change the behavior of a child component without having to look for the state or re-rendering the component. ... When a child component needs to refer to its parent's current node, the parent component must have a way for the child to receive its ref. The technique is known as ref forwarding.

#### 24.	Redux component 
There are three building parts: actions, store, and reducers.
https://blog.logrocket.com/why-use-redux-reasons-with-clear-examples-d21bffd5835/#:~:text=There%20are%20three%20building%20parts,but%20this%20time%20in%20Redux.
