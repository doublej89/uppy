---
type: docs
order: 31
title: "Dropbox"
module: "@uppy/dropbox"
permalink: docs/dropbox/
---

The `@uppy/dropbox` plugin lets users import files their Dropbox account.

An Uppy Server instance is required for the Dropbox plugin to work. Uppy Server handles authentication with Dropbox, downloads the files, and uploads them to the destination. This saves the user bandwidth, especially helpful if they are on a mobile connection.

```js
const Dropbox = require('@uppy/dropbox')

uppy.use(Dropbox, {
  // Options
})
```

[Try live!](/examples/dashboard/)

## Installation

This plugin is published as the `@uppy/dropbox` package.

```shell
npm install @uppy/dropbox
```

In the [CDN package](/docs/#With-a-script-tag), it is available on the `Uppy` global object:

```js
const Dropbox = Uppy.Dropbox
```

## Options

```js
uppy.use(Dropbox, {
  target: Dashboard,
  serverUrl: 'https://server.uppy.io/',
})
```

### `id: 'Dropbox'`

A unique identifier for this plugin. Defaults to `'Dropbox'`.

### `target: null`

DOM element, CSS selector, or plugin to mount the Dropbox provider into. This should normally be the Dashboard.

### `serverUrl: null`

URL to an [Uppy Server](/docs/server) instance.

### `serverHeaders: {}`

Custom headers that should be sent along to [Uppy Server](/docs/server) on every request.

### `serverPattern: serverUrl`

The valid and authorised URL(s) from which OAuth responses should be accepted.

This value can be a `String`, a `Regex` pattern, or an `Array` of both.

This is useful when you have your [Uppy Server](/docs/server) running on multiple hosts. Otherwise the default value should do just fine.

### `locale: {}`

Localize text that is shown to the user.

The default English strings are:

```js
strings: {
  // TODO
}
```