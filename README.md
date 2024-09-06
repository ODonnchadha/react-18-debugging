# Getting Started with the React Bug Shop Demo

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/kamranayub/pluralsight-course-react-debugging)

The fastest way to jump into the demo experience and solve the challenges is by running in the GitHub Codespace which is a preconfigured development environment with everything you need to follow along with the course.

Once you're in, simply run:

    npm start

To start the dev server, and Codespaces will prompt you to open a hosted URL in the browser to view the app.

Alternatively, you can clone the project locally and configure your own local dev environment.

## Solving the Challenges

The goal is to catch all the bugs in the shop. Each bug comes with a set of checks you need to make pass. You'll need to refactor and update the code.

The videos in the course provide the solutions to each challenge but there are often multiple ways to solve a problem with React. If you're stuck, reference the videos or explore on your own!

---

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)


## React 18 Debugging Playbook

- OVERVIEW:
    - This course will teach you how to quickly diagnose common issues using the React Developer Tools so you can spend more time writing your application.
    - Prerequisites: Functional components. Hooks. Managed state.

- INTRODUCING REACT DEVELOPER TOOLS:
    - React developer tools help understand the runtime state of your app.
    - Dev tools: Officially maintained. Open source. They do not transmit.
    - Interface:
        - Options and settings: Customize.
        - Components: Virtual DOM and runtime state.
        - Profiling: Capture performance and timeline.
    - When would you leverage the react-devtools package?
        - React Native. Safari or other extensionless browsers. 
        - Mobile browsers or embedded webview. INside a frame. Group policy requirements.
        ```javascript
            npm install -g react-devtools
            yarn add global react-devtools
            npx react-devtools
            npm install --save-dev react-devtools
        ```
        ```htm
            <html>
                <head>
                    <script src="http://localhost:8097"></script>
        ```
        ```javascript
            react-devtools
        ```
        - Standalone version. Local machine only.
        - Note: __REACT_DEVTOOLS_GLOBAL_HOOK__

- INSPECT USING THE COMPONENTS TREE:
    - Correlating HTML with Virtual DOM:
        - Understand the Components tree view:
            - Split pane: (R) Virtual DOM Tree. (L) Component details.
                - Double-click the component to `pin` it to the pane.
            - Rendering stack is *not* the trail of parent/child relationships.
                - Breadcrumb represents the render tree.
                - <> takes us to the component source code.
                - Right-click and `Reveal in sidebar` Source map folders. Virtual.
        - View component source code in the browser script debugger:
        - Find associated component for a rendered HTML element:
            - Filter within: e.g.: ^Styled
            - You can only edit useState hook values and props.
        - Find rendered HTML element for a component:
        - Log component data to the console:
    - Traversing the component treee quickly.
    - Manipulating props and state at runtime.
    - Demystifying hook indices and naming.
        - useBugNet(). useState().
        - React tracks hooks in the order that they are invoked.
        - Hook index. Starting at one per each component.
        - Only hooks that have internal state need to be tracked.
        - "Always parse hook names from source."
    - Making production debugging easier.
        - Minified code?
            ```javascript
                AppHeader.displayName = "AppHeader";
            ```

- DEBUG USING THE COMPONENTS TREE:
    - 

- WORK WITH PROFILING SESSIONS:

- DEBUG PERFORMANCE WITH FLAMEGRAPHS:

- DEBUG SCHEDULING WITH THE TIMELINE:

