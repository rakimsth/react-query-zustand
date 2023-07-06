#### Description

This is a repository for a project where I am demonstrating how to use React-Query and Zustand.

Features includes:

1. Github API call using axios and react query
2. Zustand for persistent state mgmt library.

- React-Query is a library for managing remote and asynchronous data fetching. Learn more at this [project](https://github.com/rakimsth/tanstack-query).
- Zustand is a small, fast and flexible state management library.

#### Notes

- Create Project: `npm create vite react-query-zustand `
- Install dependencies: `npm i @tanstack/react-query react-query axios`
- create the global store

```js
import { create } from "zustand";
import { persist } from "zustand/middleware";

const useGlobalStore = create(
  persist( //👈 middleware
    (set) => ({
      value: [],// 👈 initial state
      fn: () => { set((state) => ({})); //👈  update state
      },
    { name: "name-storage" } //👈 Localstorage
  )
);

```

#### Project Stack

\#React, \#React-Query, \#Zustand, \#GithubAPI, \#axios

#### Project status

- [ ] Design UI/UX
- [x] Create React App ( Vite )
- [x] Create Custom Hook
- [x] Add React-Query
- [x] Add Zustand
- [x] Create a Global Store using Zustand
