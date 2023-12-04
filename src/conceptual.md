### Conceptual Exercise

Answer the following questions below:
a library for state management. Useful for managing large applications with a lot of state.
Helps solves the issue of prop-drilling. Commonly used w/ React but doesnt need to always.
- What is Redux? Why might you use it?

- What are three features of the Redux developer tool in Chrome?
debug your react-redux app
- What is a store?
Is a centralized place where state is stored. You cannot create a store without specifying how to define initial state.
- What is a reducer?
Reducers are functions. They accept 2 objects: a state and an action. They use the action to produce and return a new state object.
Reducers must be pure functions.
- What is an action?
Redux actions ares imple instructions that tell reducers how to adjust state. They are objects and contain a type key.
Type is a by convention a string in UPPER_SNAKE_CASE
- What is an action creator?
An action creator is just an object. Example type: "SOME_ACTION", payload: "some value"
- How does data flow in a React/Redux application?
From dispatch(current state action) --> Reducer --> New State/Store
You call store.dispatch(action), Redux store calls the reducer function you gave it,
Root reducer may combine output of multiple reducers into single state tree. Redux store saves the complete state tree returned by the root reducer.
- What is the purpose of the `<Provider>` component?
Provider accepts a prop of a redux store, and we should wrap our top level App component in a Provider.
- What is the purpose of the `useSelector` hook? What does it return?
You can access values from the store with the useSelector hook. useSelector accepts a callback.
- Describe the `useDispatch` hook. What do you use it for?
useDispatch lets us dispatch actions to the store.
- What is redux-thunk and why would you use it?
redux-thunk is a middleware with a method to have more powerful actions. Dispatch actions asynchronously.
- What are propTypes?
 React components use a special property called propTypes to set up type checking: When props are passed to a React component, they are checked against the type definitions configured in the propTypes property.
- Describe the `useCallback` hook.  What is it used for?
The React useCallback Hook returns a memoized callback function. This allows us to isolate resource intensive functions so that they will not automatically run on every render. The useCallback Hook only runs when one of its dependencies update. This can improve performance.
- Compare and contrast the `useReducer` hook with Redux (including react-redux).  Why would you choose one over the other?useReducer is a built-in React hook that provides an alternative to Redux for managing state in React applications. It follows the same principles as Redux and provides a way to manage state in a predictable and scalable way.The useReducer hook takes two arguments – a reducer function and an initial state. The reducer function is responsible for updating the state based on the actions dispatched by the application. When an action is dispatched, the reducer function receives the current state and the action as arguments and returns the updated state.

useReducer is that it allows for complex state updates that may involve multiple values or objects

Redux is a popular state management library for React applications. It follows a centralized store pattern, where all application state is stored in a single object called the “store.” Any component can access this state, and any changes to the state must go through a set of predefined rules.The createStore function creates a Redux store that holds the complete state tree of your app. 

Redux has more powerful features for handling complex state management, such as middleware and the ability to combine reducers.
When it comes to scalability, Redux has a clear advantage. 

Some developers prefer the simplicity of useReducer, while others prefer the additional features and capabilities of Redux.