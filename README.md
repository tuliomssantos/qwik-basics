# Qwik

Qwik is a framework for building web applications. Qwik is built on top of [Vite](https://vitejs.dev/), and is designed to be a lightweight framework that can be used with any framework or library.

## Todo

- [ ] [Authentication](https://github.com/wmalarski/qwik-authjs-example)
- [ ] Recursive components
- [ ] Inversion Control (DI)
- [ ] Form Validation
- [ ] Charts using some react charting library

## Notes

- [Tutorial](https://qwik.builder.io/tutorial/introduction/component/)
- [Qwik / React](https://qwik.builder.io/docs/cheat/qwik-react/)
- [QwikReact allows you to use React components in Qwik](https://qwik.builder.io/integrations/react/), including the whole ecosystem of component libraries, such as Material UI, Threejs and React Spring.
- Functions are not serializable.
- [Cloudflare Workers and micro-frontends: made for one another](https://blog.cloudflare.com/better-micro-frontends/)

```
Did you mean to wrap it in `$()`?

const handleClick$ = $(
  () => void
);

# Check out https://qwik.builder.io/docs/advanced/dollar/ for more details.eslintqwik/valid-lexical-scope
```

- [Events](https://qwik.builder.io/docs/components/events/)

# Qwik City App ⚡️

- [Qwik Docs](https://qwik.builder.io/)
- [Discord](https://qwik.builder.io/chat)
- [Qwik GitHub](https://github.com/BuilderIO/qwik)
- [@QwikDev](https://twitter.com/QwikDev)
- [Vite](https://vitejs.dev/)

---

## Project Structure

This project is using Qwik with [QwikCity](https://qwik.builder.io/qwikcity/overview/). QwikCity is just a extra set of tools on top of Qwik to make it easier to build a full site, including directory-based routing, layouts, and more.

Inside your project, you'll see the following directory structure:

```
├── public/
│   └── ...
└── src/
    ├── components/
    │   └── ...
    └── routes/
        └── ...
```

- `src/routes`: Provides the directory based routing, which can include a hierarchy of `layout.tsx` layout files, and an `index.tsx` file as the page. Additionally, `index.ts` files are endpoints. Please see the [routing docs](https://qwik.builder.io/qwikcity/routing/overview/) for more info.

- `src/components`: Recommended directory for components.

- `public`: Any static assets, like images, can be placed in the public directory. Please see the [Vite public directory](https://vitejs.dev/guide/assets.html#the-public-directory) for more info.

## Add Integrations and deployment

Use the `npm run qwik add` command to add additional integrations. Some examples of integrations include: Cloudflare, Netlify or Express server, and the [Static Site Generator (SSG)](https://qwik.builder.io/qwikcity/guides/static-site-generation/).

```shell
npm run qwik add # or `yarn qwik add`
```

## Development

Development mode uses [Vite's development server](https://vitejs.dev/). During development, the `dev` command will server-side render (SSR) the output.

```shell
npm start # or `yarn start`
```

> Note: during dev mode, Vite may request a significant number of `.js` files. This does not represent a Qwik production build.

## Preview

The preview command will create a production build of the client modules, a production build of `src/entry.preview.tsx`, and run a local server. The preview server is only for convenience to locally preview a production build, and it should not be used as a production server.

```shell
npm run preview # or `yarn preview`
```

## Production

The production build will generate client and server modules by running both client and server build commands. Additionally, the build command will use Typescript to run a type check on the source code.

```shell
npm run build # or `yarn build`
```
