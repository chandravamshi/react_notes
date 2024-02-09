# React Notes
My Understanding of React and Learning Notes

---
## Table of Contents
* [Basic short intro to React](#basic-short-intro-to-react)
* [Introduction to React](#introduction-to-react)
* [Breaking User Interfaces into Smaller, Reusable Components](#breaking-user-interfaces-into-smaller-reusable-components-1)
* [How React's Virtual DOM Works](#how-reacts-virtual-dom-works)
* [JSX](#jsx)
* [Creating and Rendering React Components](#creating-and-rendering-react-components)

---

Sure, here's a rewritten version of your understanding of React and the notes you took during the learning process:

---

## Basic short intro to React
1. **Introduction to React:**
   - React is a JavaScript library for building user interfaces.
   - It allows us to create reusable UI components that update efficiently when data changes.
   - React uses a virtual DOM to improve performance by minimizing the number of changes to the actual DOM.

2. **Components:**
   - Components are the building blocks of React applications.
   - They can be either functional components or class components.
   - Functional components are simple functions that return JSX.
   - Class components are ES6 classes that extend React.Component and have a render method.

3. **JSX (JavaScript XML):**
   - JSX is a syntax extension for JavaScript that allows us to write HTML-like code within JavaScript.
   - It makes React code more readable and easier to write.

4. **State and Props:**
   - State is an object that represents the parts of a component that can change over time.
   - Props (short for properties) are inputs to a React component.
   - State is managed internally by the component, while props are passed from parent to child components.

5. **Lifecycle Methods:**
   - Lifecycle methods are special methods that are automatically invoked at various stages in the life cycle of a React component.
   - They allow us to perform actions such as initializing state, fetching data, and updating the DOM in response to changes.

6. **Handling Events:**
   - React uses synthetic events to handle DOM events in a cross-browser-compatible way.
   - Event handlers in React are written in camelCase, e.g., onClick instead of onclick.

7. **Hooks:**
   - Hooks are functions that let us use state and other React features without writing a class.
   - They were introduced in React 16.8 to allow functional components to have state and lifecycle methods.

8. **Notes:**
   - Make sure to break down the UI into reusable components for better maintainability.
   - Practice using state and props effectively to manage data flow within components.
   - Experiment with different lifecycle methods to understand when they are invoked and how they can be used.
   - Explore the latest features and best practices in React, such as hooks and context API.

Overall, React provides a powerful and efficient way to build dynamic and interactive user interfaces, and mastering its core concepts is essential for becoming a proficient in react.


---

## Introduction to React

Welcome to the world of React! In this guide, we'll explore the basics of React, including what it is, why it's used, its advantages, and how to get started with it.

### What is React?

React is a JavaScript library for building user interfaces. It allows you to create reusable UI components that efficiently update and render in response to data changes. Developed by Facebook and maintained by a community of developers, React simplifies the process of building complex user interfaces by breaking them down into smaller, reusable components.

### Why use React?

React makes it easier to develop interactive user interfaces by breaking them down into smaller, reusable components. It efficiently updates and renders components, resulting in faster performance and a better user experience. Its component-based architecture promotes code reusability and maintainability, while its virtual DOM implementation improves performance by minimizing DOM manipulations.

### Breaking User Interfaces into Smaller, Reusable Components:

Imagine you're building a house. Instead of building the entire house all at once, you break it down into smaller parts like rooms, walls, doors, and windows. Similarly, in React, you break down your user interface into smaller pieces called components. Each component represents a specific part of your UI, like a button, a form, or a header. These components can be reused throughout your application, just like using the same type of door in different rooms of a house. This makes your code easier to manage, update, and maintain.

### Efficiently Updating and Rendering Components:

When something changes in your application, React knows exactly which components need to be updated and re-rendered. Imagine you're playing a video game, and you pick up a new item. Only the part of the screen showing your inventory needs to change, not the entire game world. Similarly, React updates only the specific components that have changed, rather than re-rendering the entire page. This makes your application faster and more responsive, providing users with a better experience.

### Advantages of React Over Other Frameworks and Libraries:

React has several advantages over other JavaScript frameworks and libraries. It promotes a component-based architecture, which encourages code reusability and maintainability. Its virtual DOM implementation also improves performance by minimizing DOM manipulations. Some advantages of React include its component reusability, virtual DOM for efficient updates, and a large ecosystem of libraries and tools. However, React also has some disadvantages, such as a steep learning curve for beginners and potential performance issues with complex applications.

### Setting up a development environment with Create React App

To set up a development environment with Create React App:

1. Install Node.js and npm on your computer if you haven't already.
2. Open your terminal or command prompt.
3. Run `npm install -g create-react-app` to install Create React App globally.
4. Navigate to the directory where you want to create your React project.
5. Run `create-react-app your-project-name` to create a new React project.
6. Navigate into your project directory with `cd your-project-name`.
7. Run `npm start` to start the development server.
8. You can now start coding your React application!

### Conclusion

React is a powerful tool for building modern, interactive web applications. By breaking down user interfaces into smaller, reusable components and efficiently updating and rendering them, React provides a better development experience and improved performance. With Create React App, setting up a development environment is quick and easy, allowing you to focus on building great applications.

---

### Breaking User Interfaces into Smaller, Reusable Components

Imagine you're building a house. Instead of building the entire house all at once, you break it down into smaller parts like rooms, walls, doors, and windows. Similarly, in React, you break down your user interface into smaller pieces called components. Each component represents a specific part of your UI, like a button, a form, or a header. These components can be reused throughout your application, just like using the same type of door in different rooms of a house. This makes your code easier to manage, update, and maintain.

### Efficiently Updating and Rendering Components

When something changes in your application, React knows exactly which components need to be updated and re-rendered. Imagine you're playing a video game, and you pick up a new item. Only the part of the screen showing your inventory needs to change, not the entire game world. Similarly, React updates only the specific components that have changed, rather than re-rendering the entire page. This makes your application faster and more responsive, providing users with a better experience.

### Advantages of React Over Other Frameworks and Libraries

Think of React as a superhero that has special powers to make your development life easier. One of its superpowers is promoting a component-based architecture. This means you can build your application by piecing together reusable components like LEGO blocks. Just like how you can build different structures with the same LEGO pieces, you can create various UIs using the same React components.

Another superpower of React is its virtual DOM (Document Object Model). Imagine you have a blueprint of your house. Instead of physically moving furniture around to see how it looks, you make changes on a virtual copy of the blueprint. Once you're happy with the layout, you apply those changes to the actual house. Similarly, React creates a virtual representation of your UI in memory, compares it to the current DOM, and only updates the parts that have changed. This minimizes the number of updates to the actual DOM, resulting in faster performance.

In summary, React simplifies the process of building interactive user interfaces by breaking them down into smaller, reusable components. It efficiently updates and renders these components, resulting in faster performance and a better user experience. Its component-based architecture promotes code reusability and maintainability, while its virtual DOM implementation improves performance by minimizing DOM manipulations.

---
### How React's Virtual DOM Works

Let's break down how React's virtual DOM works step by step, using a simple example:

1. **Understanding the DOM:** The DOM (Document Object Model) is a representation of the structure of a web page. Think of it as a tree-like structure where each element (like `<div>`, `<p>`, `<span>`, etc.) is a node in the tree.

2. **Traditional DOM Manipulation:** In traditional web development, when you update something on a web page, the browser directly manipulates the DOM. For example, if you change the text of a paragraph (`<p>`), the browser updates that paragraph in the DOM, which can be slow and inefficient, especially for complex UIs.

3. **Introducing the Virtual DOM:** React introduces a concept called the virtual DOM. It's like a lightweight copy of the real DOM that React keeps in memory.

4. **Rendering Components to the Virtual DOM:** When you write React code, you create components that represent parts of your UI. When these components render, they don't directly update the real DOM. Instead, they update the virtual DOM.

5. **Diffing and Reconciliation:** After a component updates the virtual DOM, React performs a process called reconciliation. It compares the virtual DOM with the previous version of the virtual DOM to determine what has changed.

6. **Identifying Changes:** React identifies the differences between the new virtual DOM and the previous one. It figures out which parts of the UI need to be updated.

7. **Updating the Real DOM Efficiently:** Once React knows what has changed, it updates only those parts of the real DOM that need to be changed. This process is much faster than directly manipulating the entire DOM.

**Example:** Let's say you have a React component that displays a counter. When you click a button, the counter increases by one.

1. Initially, React renders the component and updates the virtual DOM with the initial counter value.
2. When you click the button, React updates the virtual DOM to reflect the new counter value.
3. React then compares the new virtual DOM with the previous one and identifies that only the counter value has changed.
4. Finally, React updates only the part of the real DOM that displays the counter, rather than re-rendering the entire page.

This process of using a virtual DOM allows React to efficiently update the UI, resulting in better performance, especially for complex applications with dynamic content.

---

### JSX 

JSX (JavaScript XML) is a syntax extension for JavaScript that allows you to write HTML-like code directly within your JavaScript files. It's not mandatory to use JSX in React, but it's a common and recommended practice because it makes your code more readable and expressive.

#### Example:

```jsx
// JSX syntax example
const element = <h1>Hello, World!</h1>;

// Transpiles to JavaScript
const element = React.createElement('h1', null, 'Hello, World!');
```

In the JSX example, `<h1>Hello, World!</h1>` looks like HTML, but it's actually JSX. When React encounters JSX, it transforms it into regular JavaScript using `React.createElement()`. The resulting JavaScript code creates a React element representing the `<h1>` with the text "Hello, World!".

Absolutely! Let's break down JSX Syntax into simple steps with examples:

#### Step 1: What is JSX?

JSX stands for JavaScript XML. It's a syntax extension for JavaScript that allows you to write HTML-like code directly within your JavaScript files. JSX makes it easier to describe what the UI should look like in React applications.

#### Step 2: How does JSX work?

In JSX, you can write HTML-like syntax within curly braces `{}`. This syntax gets transformed into regular JavaScript code using a transpiler like Babel before it's interpreted by the browser.

#### Step 3: Understanding JSX Elements

In JSX, you can create elements similar to HTML elements. For example:

```jsx
const element = <h1>Hello, World!</h1>;
```

In this example, `<h1>Hello, World!</h1>` is a JSX element representing a heading with the text "Hello, World!". This JSX syntax is transformed into regular JavaScript code by React behind the scenes.

#### Step 4: Embedding JavaScript Expressions in JSX

You can embed JavaScript expressions within curly braces `{}` in JSX. For example:

```jsx
const name = 'John';
const element = <h1>Hello, {name}!</h1>;
```

In this example, `{name}` is a JavaScript expression that gets evaluated and inserted into the JSX element. The resulting element would be `<h1>Hello, John!</h1>`.

#### Step 5: JSX Attributes

In JSX, you can also specify HTML attributes just like you would in HTML. For example:

```jsx
const element = <a href="https://www.example.com">Click here</a>;
```

In this example, `href="https://www.example.com"` is an attribute of the `<a>` element.

#### Step 6: JSX and JavaScript Objects

JSX can also accept JavaScript objects as attributes. For example:

```jsx
const attrs = {
  className: 'btn',
  onClick: handleClick
};

const button = <button {...attrs}>Click me</button>;
```

In this example, `...attrs` spreads the properties of the `attrs` object as attributes of the `<button>` element.

#### Example:

Putting it all together:

```jsx
const name = 'John';
const element = (
  <div>
    <h1>Hello, {name}!</h1>
    <p>Welcome to our website.</p>
  </div>
);
```

In this example, `element` is a JSX element representing a `<div>` containing an `<h1>` heading with the text "Hello, John!" and a `<p>` paragraph with the text "Welcome to our website.".

#### Summary:

- JSX is a syntax extension for JavaScript that allows you to write HTML-like code within your JavaScript files.
- JSX elements are transformed into regular JavaScript code before being interpreted by the browser.
- You can embed JavaScript expressions and use HTML attributes in JSX.
- JSX makes it easier to describe the UI in React applications.

---

## Creating and Rendering React Components

In React, components are reusable, self-contained building blocks for your UI. There are two main types of components: functional components and class components.

#### Functional Components:

Functional components are JavaScript functions that accept props as arguments and return JSX elements. They are simpler and more lightweight than class components, making them ideal for presentational components that don't need state or lifecycle methods.

#### Example:

```jsx
// Functional Component Example
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

// Rendering the Component
ReactDOM.render(
  <Greeting name="John" />,
  document.getElementById('root')
);
```

In this example, `Greeting` is a functional component that accepts a `name` prop and returns an `<h1>` element with a greeting message.

#### Class Components:

Class components are ES6 classes that extend `React.Component`. They have additional features like state and lifecycle methods, making them suitable for more complex components that need to manage their own state or perform side effects.

#### Example:

```jsx
// Class Component Example
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}
```

In this example, `Greeting` is a class component that also accepts a `name` prop and returns an `<h1>` element with a greeting message. The `render()` method is required in class components and returns the JSX to be rendered.

#### Mored Detailed Explanation

#### Step 1: Understanding React Components

In React, components are like custom HTML elements that you can create and use to build your UI. They encapsulate the UI logic and can be reused throughout your application.

#### Step 2: Functional Components

Functional components are JavaScript functions that accept props (properties) as arguments and return JSX (JavaScript XML) elements. They are the simplest type of component and are primarily used for presentational purposes.

#### Example:

```jsx
// Functional Component
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

#### Step 3: Rendering Components

Once you've defined a component, you can render it by including it in the JSX of another component or in the `ReactDOM.render()` method.

#### Example:

```jsx
// Rendering the Component
ReactDOM.render(
  <Greeting name="John" />,
  document.getElementById('root')
);
```

In this example, we're rendering the `Greeting` component and passing the `name` prop with the value `"John"`.

#### Step 4: Class Components

Class components are ES6 classes that extend `React.Component`. They have additional features like state and lifecycle methods, making them suitable for more complex components.

#### Example:

```jsx
// Class Component
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}
```

#### Step 5: Behind the Scenes - Component Rendering

When a component is rendered, React calls its `render()` method to generate the JSX representation of the component. This JSX is then transformed into a React element, which is ultimately rendered to the DOM.

#### Step 6: Props and State

Props are read-only properties passed to a component from its parent. They allow you to pass data from one component to another. State, on the other hand, is mutable and managed internally by the component. It represents the component's internal state and can be changed over time.

#### Step 7: Functional Components vs. Class Components

Functional components are simpler and primarily used for presentational purposes, while class components are more powerful and used for complex components that require state or lifecycle methods.

#### Summary:

- React components are like custom HTML elements used to build the UI.
- Functional components are simple JavaScript functions that return JSX elements.
- Class components are ES6 classes that extend `React.Component` and have additional features like state and lifecycle methods.
- Components are rendered by including them in the JSX of another component or using `ReactDOM.render()`.

---
## What are hooks and why hooks ?
It is a new feature from react 16.8 which allow you to use react features without writing a class.  
ex : state of component  
hooks don't work inside a class.  
#### why hooks?  
no need to create a class components.  
it will hlep to avoid the whole confusion with this keyword as you no longer use class components while using hooks.   
no need to bind event handlers like in class components.  
makes easy to share stat of the componets with other components.  
related code can be organized in one place.  
allow you to use reuse stateful logic.  
more readable and sufficient code accomplished using FC hooks.

#### Rules of hooks
only call hooks in top level of FC and any javascript funciton.  
don't call hooks in loops, condition or nested fucntions  


## hooks
###  useState
It is most common hook used. used to update a varialbe with simple steps.  
retuts a variable with initial value if given and function to udpate the varible.
* Example 1  
`const [count, setCount] = useState(0)`  
in the above code snippet count is a varialbe with intial value of 0 and setCount is a function.  
here count is a variable   
setCount is function 
`setCount` is a function which takes a callback function.  
`setCount((prevValue) => prevVlue +1)`  in this setCount will set the value to 1  
* Example 2 with object  
  `const [obj, setObj] = useState({firstName:'',lastName:''})`  
  `setObj({...obj, firstName:'Mynam'})` here `...obj` is spread spreading the obj valeus and overriding the firstName. If you don't spread the value of obj will have only `firstName`. same goes with arrays.

###  useEffect
used to perform side effects in FC.  
it is almost a replacement for componentDidUpdate,componentDidMount, componentDidUnmount in Class Component.  
runs after every render if no dependencies were given, renders when value of dependencies changes. will also have function insdie to run only before component will be unmounted. if empty array of dependencies provided runs only once only after component mounts.
return function is runned before component unmounts.

```
const [test, useTest] = useState(0)  

useEffect(
()=>{ // perfome something whenever test value changes}
 return () => 
 {
 // perform when component will unmount
} , [test] )
```   
###  useContext
In simple words, if you want to send variables through mutliple nested components we can use useContext.  
instead of sending variables as props to components you can simply use useContext hook.  
useContext provdes a way to pass data through component tree without passing data at each level of the tree.  
```
// firt create a Context
export const TestContext = React.createContext()  

// wrap a component with testContext provider
<TestContext.Provider value = {'testValue'}>
<ExampleComponet/>
<TestContext.Provider/>  

// Inside ExampleComponet
const testContext = useContext(TestContext)
return <div>{testContext}</div> // output testValue
```

##  TODO
### useRef 
### useMemo 
### useCallback 
### useLayoutEffect
### useImperativeHandle






  
