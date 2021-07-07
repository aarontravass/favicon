<div align="center">

# repo-template

[![npm][npm-img]][npm-url] [![GitHub Workflow Status][gh-actions-img]][github-actions] [![Coverage][cov-img]][cov-url]

</div>

Description.

> A rewrite of [serve-favicon](https://github.com/expressjs/serve-favicon) module.

Node.js middleware to serve `favicon.ico` file.

## Install

```sh
pnpm i @tinyhttp/favicon
```

## API

```js
import { favicon } from '@tinyhttp/favicon'
```

### Options

`favicon` accepts these properties in the options object.

#### `path`

Path to icon, required. Passed as the first argument.

#### `maxAge`

Sets `Cache-Control: maxAge=` header, optional. Default is one year. Passed with object in the second argument.

## Example

```js
import { favicon } from '@tinyhttp/favicon'
import { createServer } from 'http'
import path from 'path'

http.createServer(favicon(path.join(process.cwd(), 'public', 'favicon.ico')).listen(3000)
```

[npm-url]: https://npmjs.com/package/@tinyhttp/favicon
[github-actions]: https://github.com/tinyhttp/favicon/actions
[gh-actions-img]: https://img.shields.io/github/workflow/status/tinyhttp/favicon/CI?style=for-the-badge&logo=github&label=
[cov-img]: https://img.shields.io/coveralls/github/tinyhttp/favicon?style=for-the-badge
[cov-url]: https://coveralls.io/github/tinyhttp/favicon
[npm-img]: https://img.shields.io/npm/dt/@tinyhttp/favicon?style=for-the-badge
