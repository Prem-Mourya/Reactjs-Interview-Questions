Q -> Virtual DOM, Fiber, and reconciliation

--> This is what you have to tell in an interview.

1. Virtual DOM
The Virtual DOM (VDOM) is a lightweight representation of the actual DOM (Document Object Model) in memory. It is a JavaScript object that React uses to optimize updates and rendering in the browser. When the state of a React component changes, React updates the Virtual DOM first and compares it with a previous snapshot (using a process called "diffing"). Only the parts of the actual DOM that have changed are updated, which improves performance.

2. Fiber
Fiber is the reimplementation of the React reconciliation algorithm introduced in React 16. It is a data structure (tree) that represents the Virtual DOM but with enhanced capabilities. React Fiber allows React to break rendering work into chunks and prioritize updates based on their importance. This enables features like time-slicing, concurrent rendering, and smooth handling of animations or transitions by pausing and resuming rendering tasks.

Key benefits of Fiber:

->Enables concurrent rendering.
->Handles interruption and prioritization of tasks.
->Improves performance for large, complex UIs.

3. Reconciliation
Reconciliation is the process React uses to update the DOM efficiently. It involves comparing the current Virtual DOM with the previous version to determine the minimal number of changes required to update the real DOM. This process is powered by the diffing algorithm, which works under two key assumptions:

Elements of different types will produce different trees.
Elements of the same type will be updated, keeping their state when possible.

Source: https://youtu.be/MPCVGFvgVEQ?si=1_UHH1C8MMQJ5khU
