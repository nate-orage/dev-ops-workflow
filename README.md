<!-- https://www.markdownguide.org/basic-syntax/ -->
# CI/CD Workflow
This is a simple Github/Travis CI workflow that deploys a node.js application to AWS. Elastic Beanstalk manages the tasks that deploy the docker application to an EC2 instance that auto-scales if demand increases.

![Workflow](./frontend/img/workflow.png 'Workflow')

## Dev Workflow
- Dev commits changes to "Feature" branch on Github.
- Travis CI detects changes and runs tests.
- If the tests pass, the dev submits a pull request to the main branch.
- Once the pull request is opened, Travis tests again.
- If the tests pass, whoever owns the main branch will approve the pull request to the main branch.
- Once the pull request is approved, Travis sends the application to AWS Elastic Beanstalk where it will manage the tasks that deploy the application.

## Contents
- `public` and `src` are files for the web application.
- `.travis.yml` contains local test commands and deployment details for AWS.
- `docker-compose-dev.yml` will build a dev environment on your local computer. You can access the web app at http://localhost:3000.
- `docker-compose.yml` is used in production.
<!-- 
## Common Docker Commands
```bash
docker images # List docker images 
docker container ls # List RUNNING docker containers
docker container ls -a # List ALL docker containers
docker container stop
docker exec -it <Container ID> /bin/bash # Access running container via bash shell.
docker container rm <Container ID> # Delete docker container. Container must be stopped.
docker rmi <Image ID> # Delete image. Image must not be present on any existing docker containers. If so, the containers must be deleted before deleting the image.
```
---

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

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify) -->
