# What are React components and how are they reused?

React components are self-contained and reusable pieces of code that define a part of the user interface. Components can be functional or class-based, although functional components with hooks are the modern standard. They accept inputs (props) and return React elements describing what should be rendered on the screen. Reusability is achieved by rendering the same component in different parts of the application or multiple times within the same view, potentially with different props. This modularity simplifies development and promotes code maintainability.

# What is state in React and how does it work under the hood?

State in React refers to data that can change over time and affects the component's rendering. It is managed internally within the component using the useState hook for functional components or the this.state property for class components. When state changes, React efficiently updates the relevant parts of the UI by comparing the virtual DOM with the actual DOM and applying only the necessary changes. Under the hood, React maintains an internal object for each component instance to track its state, and updates trigger a re-render of the component and its children.

# What is "lifting state up" and when should you use it?

"Lifting state up" involves moving state management from a child component to a common ancestor component. This is necessary when multiple components need to share and modify the same data. By lifting the state up, the shared data and the functions that update it are centralized in a parent component, which then passes them down as props to the child components. This pattern ensures data consistency and avoids prop drilling, where data has to be passed through multiple levels of components that don't need it. It should be used when data needs to be accessed and modified by multiple components.

# What are keys in lists, and why are they important in React?

Keys in lists are special string attributes assigned to elements when rendering collections of items in React. They provide a stable identity for each item, allowing React to efficiently update, add, or remove elements in the list without re-rendering the entire list. Without keys, React might unnecessarily re-render elements, leading to performance issues, especially in complex lists with frequent updates. Keys should be unique and ideally based on a stable identifier from the data, such as an ID or unique name.