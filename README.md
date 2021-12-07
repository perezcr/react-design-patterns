# React: Design Patterns

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Layout Components

Layout components are components in React that deal primarily with arranging other components on the page. Some examples of this that you're probably familiar with are split screens, so arranging more than one component in different sections of the page. We also have lists and items, so displaying data in a list. And modals, is just content that gets displayed over top of the actual page.

<p align="center">
  <img src="img/1.png" alt="Layout Components">
</p>

The main idea of layout components is that our components that we create, the main content components of our pages, shouldn't know or care where they're actually being displayed on the page.

## Container Components

Container components are basically React components that take care of all of the data loading and other data management for their child components.

Let's imagine that we have a container component with several child components inside of it. Normally what you would do, is you would just have each of those child components load their own data and then display it. So up where it says low data, you probably have a useState hook and a useEffect hook and use something like Axios or Fetch to get data from a server. Now, the problem with this is that a lot of the time we need our child components to be able to share that logic. And the way that container components solve that problem is by splitting that logic out into its own component, which is the container and the container then takes care of loading that data and passes it automatically to the children components.

<p align="center">
  <img src="img/2.png" alt="Container Components">
</p>

So the main idea with container components, we don't want our components to know where their data is coming from or how to manage it. We just want our components to be dumb and take some props and display whatever they need to display.

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.
