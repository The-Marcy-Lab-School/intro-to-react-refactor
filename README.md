# Intro to React Simple Refactor Lab

For this exercise, you'll be practicing using `create-react-app` as a scaffolding toolchain. You'll be using the components your created last lab. 

## Set Up

Following the [Create React App Instructions](https://reactjs.org/docs/create-a-new-react-app.html) to create a new react project. Open the project in a code editor and inspect the `package.json`. Pay special attention to the scripts (`npm start`) and which dependencies were downloaded. Examine the other files in the project. There may be some code your are not familiar with, and that's ok. Pay special attention to `index.js`.

## Creating Components

Your starter code renders an `App` component. You will be creating all other components, so go ahead and remove all the HTML tags rendered by `App`. We will have our `App` render a `NavBar`, `Header`, and `CardContainer` components instead.

### Header

Re-create the `Header` component from your last lab. A `Header` takes in a prop of `title` and should renders that title as an `h1` tag. Make sure the `Header` component lives in its own file. Finally, your `App` component should render a `Header` (pass any title you want).

### NavBar

Re-create the `NavBar` component from your last lab. A `NavBar` takes in an array props called `pages` like below:

```js
const pageData = [{text: "About", link: "/about"}, {text: "Our Team", link: "/team"}, {text: "Pricing", link: "/pricing"}];
<NavBar pages={pageData} />
```

It should display an unordered list of page links. Again, make sure `NavBar` lives in its own file.  Finally, your `App` component should render a `NavBar` _before_ it renders a `Header`.

### Card

Re-create the `Card` component from your last lab. A `Card` takes in the following props: `level` (number), `points` (number), `image` (string) and `name` (string). It should live in its own file and display information basked on [this mockup](https://github.com/The-Marcy-Lab-School/review-8_0/blob/master/card.png).


### CardContainer

In React, it's often useful to create **Container Components**, a component whose sole purpose is to contain other components. **Presentational Components** on the other hand are uses to display things. You can read about [Presentational and Container Components](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0) here.

Create a `CardContainer` component which lives in it's own file. In your `CardContainer.js`, create an array of `users` where each user has a name, image, level, and points. Feel free to copy the example below into your code:

```js
const users = [
  {name: "Helen Doe", image: "https://semantic-ui.com/images/avatar/large/helen.jpg", level: 4, points: 2435}, 
  {name: "Daniel Rodriguez", image: "https://semantic-ui.com/images/avatar/large/daniel.jpg", level: 13, points: 5235}, 
  {name: "Joe Jones", image: "https://semantic-ui.com/images/avatar/large/joe.jpg", level: 20, points: 10513}
]
```

Your `CardContainer` component should render a `Card` for each user. Think about what iterator method you'll want to use. Do not hard code the number of `Card`s. If the length of the `users` array changes, then `CardContainer` should render more or less `Card` components respectively. Finally, the `CardContainer` component should be _rendered by_ the `App` component.

## Component Hierarchy

Your UI should render all your components onto the page. The component hierarchy should be something like:
```
App
 |- NavBar
 |- Header
 |- CardContainer
      |- Card
      |- Card
      |- Card
```

When you are finished push up your code to Github and submit the URL of your repo to Canvas. 
