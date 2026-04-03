# @stzhu/tsconfig

## Installation

```bash
pnpm i -D @stzhu/tsconfig
```

## Usage

After installation, extend the relevant configuration in your `tsconfig.json`.

```json
{
  "extends": "@stzhu/tsconfig/tsconfig.react.json"
}
```

## Configs

### `tsconfig.base.json`

Shared base config with strict type-checking and modern defaults. Not intended to be used directly — extend one of the configs below instead.

### `tsconfig.node.json`

For Node.js projects. Uses `nodenext` module resolution and `erasableSyntaxOnly` for compatibility with Node's native TypeScript support.

### `tsconfig.bun.json`

For Bun projects. Uses `bundler` module resolution with `module: "preserve"`.

### `tsconfig.lib.json`

For libraries built with a bundler (e.g. tsup, Vite library mode). Uses `bundler` module resolution with `module: "preserve"`. Similar to the Bun config but without `lib: ["ESNext"]` so consumers can set their own lib target.

### `tsconfig.react.json`

For React projects built with a bundler (e.g. Vite, Next.js). Extends the bundler setup with `jsx: "react-jsx"`.
