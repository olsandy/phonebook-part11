# Osa 3 - puhelinluettelo backend

## Usage

### Current deployment

The app is currently built and deployed at [https://fso-palautukset-osa3.onrender.com/](https://fso-palautukset-osa3.onrender.com/).

### Installation

Use the package manager npm to install the project.

```bash
npm install
```

The app uses [Mongo DB Atlas](https://www.mongodb.com/atlas/database) as the database. Register to the service and create a file named `.env` to the root of your project with content (replacing the username, password, connection string and database names)

```bash
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.o1opl.mongodb.net/phoneBookApp?retryWrites=true&w=majority
PORT=3001
```

To build the app

```bash
npm run build:ui
```

Note that the build script assumes that the source code for fullstack open Part 2 is located at `~/git/fullstackopen-palautukset/osa2/puhelinluettelo/`. Change it to something suitable in the `package.json` file at `build:ui`.

Run locally
```bash
npm start
```

Deployment is done by pushing the changes to `git`. [Render](https://dashboard.render.com/) can be configured to listen to your deployment branch by web hook and automatically deploy the latest commit. You need to add an environment variable `MONGODB_URI` to the Render dashboard for the database connection. 

A script is defined in `package.json` for building and deploying:

```bash
npm run deploy:full
```