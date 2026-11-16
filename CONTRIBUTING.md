# 📖 Guidelines

-   If the existing tests do not already cover your changes, please add tests.
-   Please run `npm run format` for formatting the code before submitting the pull request.

# ⚒️ Developing the Action code

## Build the code

If you'd like to help us develop and enhance this Action, this section is for you.

The Action ships its bundled output from `dist/` - the dependencies are not committed as `node_modules`, so the sources must be bundled before submitting a pull request:

```bash
npm i && npm run bundle
```

`npm run bundle` compiles the TypeScript sources and regenerates `dist/main/index.js` and `dist/cleanup/index.js`. Commit the regenerated `dist/` files together with your changes - CI fails when the committed bundle is out of date.

To run the Action tests, run

```bash
npm t
```
