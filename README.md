<div align="center">
    <img src="tossr_logo.svg" alt="tossr" width="400" /><br>
</div>

### Universal SPA to SSR

Render HTML from any SPA.

### Install

`npm i tossr`

### Usage example

```javascript
const { tossr } = require('tossr')

const template = 'dist/index.html'
const script = 'dist/app.js'
const url = '/blog/ssr-is-fun'

const html = await tossr(template, script, url)
```

### Related libraries

-   [Spassr](https://github.com/roxiness/spassr) Small Express server with built in SSR
-   [Spank](https://github.com/roxiness/spank) Generate a static site from any SPA

* * *

### API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

##### Table of Contents

-   [tossr](#tossr)
    -   [Parameters](#parameters)
-   [Config](#config)
    -   [Properties](#properties)
-   [Eval](#eval)
    -   [Parameters](#parameters-1)

#### tossr

Renders an HTML page from a HTML template, an app bundle and a path

##### Parameters

-   `template` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Html template (or path to a HTML template).
-   `script` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Bundled JS app (or path to bundled bundle JS app).
-   `url` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Path to render. Ie. /blog/breathing-oxygen-linked-to-staying-alive
-   `options` **Partial&lt;[Config](#config)>?** Options

Returns **[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)>** 

#### Config

Type: [object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)

##### Properties

-   `host` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** hostname to use while rendering. Defaults to <http://jsdom.ssr>
-   `eventName` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** event to wait for before rendering app. Defaults to 'app-loaded'
-   `beforeEval` **[Eval](#eval)** Executed before script is evaluated.
-   `afterEval` **[Eval](#eval)** Executed after script is evaluated.
-   `silent` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** Don't print timestamps
-   `inlineDynamicImports` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** required for apps with dynamic imports
-   `timeout` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** required for apps with dynamic imports
-   `dev` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** disables caching of inlinedDynamicImports bundle
-   `errorHandler` **[function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)** 

#### Eval

Called before/after the app script is evaluated

Type: [Function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)

##### Parameters

-   `dom` **[object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** The DOM object
    \*


---

<a href="https://www.freepik.com/vectors/party">Party vector created by gstudioimagen - www.freepik.com</a>
