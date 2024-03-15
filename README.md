remark-github-alert
===
<!--rehype:style=display: flex; height: 230px; align-items: center; justify-content: center; font-size: 38px;-->

[![Buy me a coffee](https://img.shields.io/badge/Buy%20me%20a%20coffee-048754?logo=buymeacoffee)](https://jaywcjlove.github.io/#/sponsor) 
[![Downloads](https://img.shields.io/npm/dm/rehype-github-alert.svg?style=flat)](https://www.npmjs.com/package/rehype-github-alert)
[![NPM version](https://img.shields.io/npm/v/rehype-github-alert.svg?style=flat)](https://npmjs.org/package/rehype-github-alert)
[![Build](https://github.com/jaywcjlove/rehype-github-alert/actions/workflows/ci.yml/badge.svg)](https://github.com/jaywcjlove/rehype-github-alert/actions/workflows/ci.yml)
[![Coverage Status](https://jaywcjlove.github.io/rehype-github-alert/badges.svg)](https://jaywcjlove.github.io/rehype-github-alert/lcov-report/)
[![Repo Dependents](https://badgen.net/github/dependents-repo/jaywcjlove/rehype-github-alert)](https://github.com/jaywcjlove/rehype-github-alert/network/dependents)

Remark plugin to add support for [GitHub Alert](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts)

Alerts are a Markdown extension based on the blockquote syntax that you can use to emphasize critical information.

## Installation

This package is [ESM only](https://gist.github.com/sindresorhus/a39789f98801d908bbc7ff3ecc99d99c): Node 12+ is needed to use it and it must be `import` instead of `require`.

```bash
npm install rehype-github-alert
```

## Usage

```js
import plugin from 'rehype-github-alert'

const html = String(
  await remark().use(remarkParse).use(plugin).use(remarkRehype).use(rehypeStringify).process(`\
# Alert
> [!NOTE]
> test
`),
)
```

The output HTML will be:

```html
<h1>Alert</h1>
<div class="markdown-alert markdown-alert-note" dir="auto">
<p class="markdown-alert-title" dir="auto"><svg class="octicon" viewBox="0 0 16 16" width="16" height="16" aria-hidden="true"><path d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8Zm8-6.5a6.5 6.5 0 1 0 0 13 6.5 6.5 0 0 0 0-13ZM6.5 7.75A.75.75 0 0 1 7.25 7h1a.75.75 0 0 1 .75.75v2.75h.25a.75.75 0 0 1 0 1.5h-2a.75.75 0 0 1 0-1.5h.25v-2h-.25a.75.75 0 0 1-.75-.75ZM8 6a1 1 0 1 1 0-2 1 1 0 0 1 0 2Z"></path></svg>NOTE</p>
<p>Useful information that users should know, even when skimming content.</p>
</div>
```


## Related

- [`rehype-rewrite`](https://github.com/jaywcjlove/rehype-rewrite) Rewrite element with rehype.
- [`rehype-video`](https://github.com/jaywcjlove/rehype-video) Add improved video syntax: links to `.mp4` and `.mov` turn into videos.
- [`rehype-attr`](https://github.com/jaywcjlove/rehype-attr) New syntax to add attributes to Markdown.
- [`rehype-ignore`](https://github.com/jaywcjlove/rehype-ignore) Ignore content display via HTML comments, Shown in GitHub readme, excluded in HTML.

## Contributors

As always, thanks to our amazing contributors!

<a href="https://github.com/jaywcjlove/remark-github-alert/graphs/contributors">
  <img src="https://jaywcjlove.github.io/remark-github-alert/CONTRIBUTORS.svg" />
</a>

Made with [contributors](https://github.com/jaywcjlove/github-action-contributors).

## License

MIT © [Kenny Wong](https://github.com/jaywcjlove)
