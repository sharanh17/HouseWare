# Getting Started with Create React App

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


//## Changes made by Sharan//#


Rendering Todo Item:
Verify that a todo item is rendered with the correct text.
Ensure that the todo item displays an unchecked checkbox indicating it's not completed.
Marking Todo Item as Completed:
Simulate a user click on the todo item's checkbox.
Verify that the todo item updates its appearance to indicate completion (e.g., checked checkbox, strikethrough text).
Deleting Todo Item:
Simulate a user click on the delete button for the todo item.
Ensure that the todo item is removed from the list.
TodoList Component:

Type of Tests: Integration Tests
Test Cases:
Rendering Todo List:
Verify that the todo list component renders a list of todo items.
Ensure that each todo item in the list corresponds to a todo item object provided as props.
Adding New Todo Item:
Simulate user input in the input field to add a new todo item.
Verify that the new todo item is added to the list and displayed correctly.
Filtering Todo Items:
Simulate user interaction with the filter buttons (e.g., All, Active, Completed).
Ensure that the todo list updates to display only the relevant todo items based on the selected filter.
Services:
TodoService:
Type of Tests: Unit Tests
Test Cases:
Fetching Todo Items:
Mock the API call to fetch todo items.
Verify that the todo items are fetched correctly from the API.
Adding New Todo Item:
Mock the API call to add a new todo item.
Verify that the new todo item is added to the API correctly.
Updating Todo Item Completion Status:
Mock the API call to update the completion status of a todo item.
Verify that the completion status of the todo item is updated correctly in the API.

eg-
test('renders todo item with correct text', () => {
  const todo = { id: 1, text: 'Test Todo', completed: false };
  const { getByText } = render(<TodoItem todo={todo} />);
  expect(getByText('Test Todo')).toBeInTheDocument();
});