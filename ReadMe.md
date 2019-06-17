[![Build Status](https://travis-ci.com/bl4ck4ndbr0wn/multi-docker.svg?branch=develop)](https://travis-ci.com/bl4ck4ndbr0wn/multi-docker)

Complex Finbonacci Application that shows multi-container deployment using docker and AWS.

## Available Scripts

In the project directory, you can run:

### `start all services`

```
docker-compose up
```

Runs the app in the development mode.<br>
Open [http://localhost:3050](http://localhost:3050) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `test client`

- step 1:

```
docker build -t alphanganga/client-test -f ./client/Dockerfile.dev ./client
```

- step 2:

```
docker run -it alphanganga/client-test npm run test -- --coverage
```

### `build client`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

```
docker build -t alphanganga/multi-client ./client
```

```
docker run -p 3000:3000 alphanganga/multi-client
```

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.
