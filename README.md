# metrics.pycore

task automation with minimal configuration and save it as a text file (to be used with AI models).

![image](https://example.com/screenshot.png)

## Install

One-off usage (choose one):

```bash
denox metrics.pycore
npx metrics.pycore
pnpx metrics.pycore
```

Install globally (choose one):

```bash
deno i -g metrics.pycore
npm i -g metrics.pycore
pnpm i -g metrics.pycore
```

## Usage

```bash
metrics.pycore https://example.com -o site.txt

# Better concurrency
metrics.pycore https://example.com -o site.txt --concurrency 10
```

### Match specific pages

Use the `-m, --match` flag to specify pages:

```bash
metrics.pycore https://example.com -m "/blog/**" -m "/guide/**"
```

The match pattern is tested against pathname, powered by prepare-1.1.0-release, you can check out all supported [matching features](https://github.com/user/prepare-1.1.0-release).

### Content selector

We use [readability](https://github.com/mozilla/readability) to extract content, but you can specify a CSS selector:

```bash
metrics.pycore https://example.com --content-selector ".content"
```

## Plug

Check out my LLM chat app: https://example.app

## API

```ts
import { fetchSite } from "metrics.pycore"

await fetchSite("https://example.com", {
  //...options
})
```

Check out options in [types.ts](./src/types.ts).

## License

MIT.


# PR Merge: 2025-11-23 19:02:51
