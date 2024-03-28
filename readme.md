# Setting up a ReactJS project using Vite

First we need to create a file named **package.json**

```
npm init -y
```

Then we install react and react-dom

```
pnpm add react and react-dom
```

Now we install vite and @vite/plugin-react in order to run a development server

```
pnpm add -D vite @vite/plugin-react
```

At this point we need create the following config file of vite **\*vite.config.js** and it is placed on the root of the project

```js
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()],
});
```

Now we are going to add Typescript to our project

```
pnpm add -D typescript
```

Now we need to install the types to react and react-dom

```
pnpm add -D @types/react @types/react-dom
```

Every project should have a formatter and linter, in this case we are going to add the next extensions to VSCode

- Prettier
- ESLint

Now we need to create a config file for prettier, the name of this file is **.prettierrc**

We need to ensure that formatter runs on our files before every commit

```
pnpm add -D prettier
```

If we want to run scripts before a commit we need to install the next dependency

```
pnpm add -D husky
```

Now it needs to be initialized

```
pnpm exec husky init
```

Also, every project needs a static checker as known as linter. We will install:

```
pnpm add -D eslint
```
