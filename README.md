# Example: PNPM monorepo

## Prerequisites

### Tools

You will need the following things properly installed on your computer.

- [Git](http://git-scm.com/downloads)
- [Node.js](http://nodejs.org/)

### PNPM install

- If you have installed latest v16.x or greater node version in your system, then enable the pnpm using the below cmd

```bash
corepack enable
corepack prepare pnpm@latest --activate
```

- If you are using lower version of node in your local system then check this page for additional installation methods https://pnpm.io/installation

## Usage

### Install packages

```
pnpm install
```

## To start both web app and common util in dev server

We need to build and watch the `common` package and run the the dev server for web app . This way whenever there is a change in the `Common` package, it will automatically reflect in the web-app.

Run the commands in different tabs in your terminal.

```
pnpm common build --watch
pnpm app dev
```

and visit http://localhost:5173

### To build the web-app

```
pnpm common build && pnpm app build
```

### To run the linter

```
pnpm lint
```

### To format the files

```
pnpm format
```
