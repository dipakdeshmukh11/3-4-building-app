# 3-4-building-app
## npm script :-

```javascript
 "scripts": {
    "start": "parcel index.html",
    "build": "parcel build index.html"
  }
```

## JSX :- html/xml like syntax

- it's html like syntax but its not html element, it is jsx convention.

- react and jsx are both different .. means jsx is not part of core React.

- our bundler has babel dependency that understand jsx & convert to ReactElement.

  ## Babel :- js compiler

- some browser does not understand newer javascript code, that time babel does take our ES6+ code and gives browser compatibilty code.

- i loves <b> Babel </b> ❤️ for doing browser compatibilty.

### Who is convert jsx to ReactElement ?

- Babel package --> manage by bundler

- Babel just takes jsx and transpile to React.createElement(). now its responsibilty of core react that gives object.

## React Component :-

- Class based component --> old way
- Functional component --> latest way

## React Functional Component :-

it's just a normal javascript function which return jsx/ ReactElement.

- behind the scene, jsx is convert to ReactElement by Babel.

- Always use PascalCase for React Function components.

### How will use Functional component :-

```javascript
// babel knows it is functional component that return jsx & convert to ReactElement which is object.

<Component />
<Component> </Component>
Component()
```

## Component Composition :-

- it means use our <b>Component inside other Component</b> called as Component Composition.

- it make your component to reuseable. --> not new thing bcz in js always function use for reuseability.

## JSX SuperPower :-

- you can put any js code inside jsx using {} to prevent from jsx.

- <h3>writing js code inside of jsx is a very powerful thing, don't underistimate. </h3>

- babel does all jsx code convert to React code 🤘

### peoples say jsx is mix of html & js ..😂

- <b> big No, jsx is html like syntax not a html</b>

## End of the Day ✅ :-

- React is js code EOD(end of day).

- ReactElement is object EOD.

- JSX is ReactElement EOD.

- Function Component is just js Function EOD.

#  Talk is cheap, Show me the code

## How the build large project :-

- Planning :

  - before writing a code, you just plan how to build app skelton

  - then writing a code is easy for you, so first build mock, wireframe.

## Note :-

- jsx is strict than html.

- in jsx, we write js code using { } and escape from jsx

### in jsx, how we look/put Inline Style :-

- <b> style = { { backgroundColor : "gray", fontSize : "24px" } } :- </b>

  - it is not inline css style, it's js object

  - first { } use for js code & prevent from jsx & another { } is object

## Design Food Ordering App :-

- Header

  - Logo
  - NavItems

- Body

  - Search
  - RestroCardContainer
    - RestroCard

- Footer
  - Copyright

## props : -

- it is short name of properties & returns object

- always pass from parent component/ element.

- EOD, props are just passing normal argument to function.

## Config Driven UI :-

- our web-app is driven by config data :-

  - it means different city have different UI , ProductCards, Caraousel & Offers

  - config data comes from backend

## How Frontend Application Builds :-

- UI Layer --> makes static website

- Data Layer --> makes dynamic web-app

### UI is Powered by Data

## key :- used for Optimization of React Cycle

- whenever you are iterate things using map() or loop, that time, pass the <b> key </b> as a prop for unique identification in React.

- When you don't pass a key in React, React Cycle re-renders everything because it doesn't recognize a unique ID.

- React recommended that never use indexes as a key, it is a bad practice.

#  Let's get Hooked

## Two types of Export & Import in React:-

- Default Export & Import :- use for only one export

  - export default Component
  - import Component from "path"

- Name Export & Import :- use for Multiple export in one component/file
  - export Component
  - import { Component, AnotherComponent } from "path"

## Can i use default export along with name export ?

- ### yes, you can but default export is only one.

## Features :-

- ### Filter of Top Rated Restraurants

## Normal Js Variables in React :-

- if we use normal js variables in react, then it don't update/modify our UI/UI State.

## State Variable :- Superpowerful local variable in react

- it is like react variable when state is updated that time it will updated our UI.

- state variables created by hooks of useState() hook.

- whenever a state variable updated , react will re-render that component & update our UI & it's so so fast

## Hooks :- Normal js Utility Functions

- hook is just normal js utility function which is given by react.

- that functions are behind the scene some logic which we use as utility function.

### useState() Hook :-

- ### useState() :- Superpowerful state variables

  - used for create local State Variables in react function component

  - it gives array of two element:-

    - initial state

    - function that updated our state automagically.
      - it needs trigger to start diff algorithm... thats why we use state variables.

## React Two Layer :-

- UI Layer

- Data Layer

- React keeps your Data layer & sync with UI layer

- when Data layer Modifiy react re-render component and quickly updated UI, bcz UI layer is Powered by Data layer

## Logic of UI Update in React ?

- ### when state updates, react will re-render of that component.

## Why React is Fast ?

- React can do fast & efficient DOM Manipulation.

- it has virtual DOM that is EOD Object.

  - Virtual DOM :- representation of an actual DOM, but it is faster than actual DOM.

- Diff algorithm :- it is difference between two virtual DOM.

  - it find difference between new virtual dom & old virtual dom & actual update DOM on every render cycle.

- React Reconciliation Algorithm / React Fiber

  - Reconciliation :- whenever something changes on ui this is known as Reconsillation.

  - React Fiber :-
    - it is Re-Implementation of React core algorithm.
    - it is new way of finding the Diff & Actually updating the DOM.
    - it is does not touch html alot
    - React Fiber comes in react 16 which year of 2017

- In short, Every Re-Rendering React will finding diff of two virtual DOM & Update the Original DOM.. thats why React is so Fast .

# Episode-6 : Exploring the World

## Monolithic vs Micro Service :- 🚀🚀

- ### single responsibilty principle :- 🚀🚀

## Real World Data :- Swiggy live API fetch for practice purpose of How Dynamic data comes in Real World

- Real World API has lot of complicated and mess up data that's why we use live swiggy api for Real World industrial practice purpose.

## useEffect() Hook :- after rendering component, it will call callback function

```javascript
useEffect(() => {
  return fetchAPI();
}, []);
```

- ### if you have to do something, after rendering the component you have write inside useEffect()

## cors policy :- 🚀🚀 Cross Origin Resource Sharing

<!-- - it is mechanism which uses additional http request header
- same origin then cors easily share resources but if two different port or different origin access resources then browser did not allow share resource.
- it is http header based mechanism that allow -->

- ### bypass cors error :- download cors chrome extension

## Shimmer UI :- use for Better UX --> first shimmer effect show, then fetch api & rerender

- Page load --> Render Shimmer/component --> fetch api --> Re-Render

- shimmer ui is a fake page skelon until the real data comes for better ux (user experience)

## Conditional Rendering :- based on conditon renders component

## why normal js variables are not use in React?

- normal js variables not update ui

  - because react will not track variables when it is update.

- thats why react gives you useState() hook which returns array & in that array two elements :-

  - initial state variable

  - function that update state and re-render component again

  - whenever state updated, that time React will Re-Render Whole Component but update only difference between two virtual dom ... so hooks are powerful things in React.

## Features :-

- Fetching Live Swiggy API ❤️
- Config Driven UI
- Searching Product
- Filter / Top Rating Product
- Shimmer UI Effect for Better User Experience (UX) ❤️
- Mobile Responsiveness
- Error Handling


## Hook :- normal js Utility Function gives by React

- dont take tension of Hooks, Hooks are normal js Utility Function that react gives you.

- useState() // initial state as a argument
- useEffect() // 2 arguments (callback fn, dependency array)
- useContext()
- useRef()
- useMemo()
- useCallback()
- useParams() provided by react-router-dom // no argument
- useRouteError() provided by react-router-dom // no argument

## useEffect() hook :- When you have to do something after rendering component

- it is Utility Function that take two elements.

  - Callback Function :- calls callback function after rendering component..

  - Dependency Array :- optional argument

    - if useEffect() hook has no dependency array, every time it will calls callback function after component render/re-renders.

    - if empty [] dependecy array, then it will call only once after component render.

    - if state [state] dependecy array, then it will call callback function whenver state updated.

## State :- React Variable

- normal js variables can't update UI.

- React will not track js variables & can't re-rendering on UI.. thats why we need of State variables.

- it is a Powerful Variables that react gives you.

- state is created by useState() hook.

## useState() hook :-

- it is utility function, that gives/return an array.

- useState() hook gives you array that have two elements :-

  - Initial State

  - Function that update state

## 🚀🚀🚀 Note :-

- Whenever State is Updated, that time Reconcillation process trigers, find diff between two virtual DOM and Whole Component is Re-Render and & that diff only updated in Actual DOM... thats why React is so fast for efficient DOM rendering.
