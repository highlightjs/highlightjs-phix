![logo](ok.ico)

# Phix - a language grammar for [highlight.js](https://highlightjs.org/)

<!--
![version](https://badgen.net/npm/v/highlightjs-cypher) ![license](https://badgen.net/badge/license/CC0%201.0/blue)
![install size](https://badgen.net/packagephobia/install/highlightjs-cypher) ![minified size](https://badgen.net/bundlephobia/min/highlightjs-cypher)
[![Build Status](https://travis-ci.com/highlightjs/highlightjs-cypher.svg?branch=master)](https://travis-ci.com/highlightjs/highlightjs-cypher)
-->

Phix is a hybrid interpreted/compiled general purpose programming language.

## Usage

Simply include the Highlight.js library in your webpage or Node app, then load this module.

### Static website or simple usage

Simply load the module after loading Highlight.js. You'll use the minified version found in the `dist` directory. This module is just a CDN build of the language, so it will register itself as the Javascript is loaded.

```html
<script type="text/javascript" src="/path/to/highlight.min.js"></script>
<script type="text/javascript" charset="UTF-8"
  src="/path/to/highlightjs-phix/dist/phix.min.js"></script>
<script type="text/javascript">
  hljs.registerLanguage("phix",hljsDefinePhix);
  hljs.highlightAll();
</script>
```

<!--
### Using directly from the UNPKG CDN (???)

```html
<script type="text/javascript"
  src="https://unpkg.com/highlightjs-phix/dist/phix.min.js"></script>
```

- More info: <https://unpkg.com>

-->
### With Node or another build system

If you're using Node / Webpack / Rollup / Browserify, etc, simply require the language module, then register it with Highlight.js.

```javascript
var hljs = require('highlightjs');
var hljsPhix = require('highlightjs-phix');

hljs.registerLanguage("phix", hljsPhix);
hljs.highlightAll();
```
<!--
### React (???)

You need to import both Highlight.js and third-party language like Phix:

```js
import React, {Component} from 'react'
import 'highlight.js/scss/darcula.scss' # your favourite theme
import phix from './phix'
import hljs from 'highlight.js'
hljs.registerLanguage('phix', phix);

class Highlighter extends Component
{
  constructor(props)
  {
    super(props);
    hljs.highlightAll();
  }

  render()
  {
    let {children} = this.props;
    return
    {
      <pre ref={(node) => this.node = node}>
        <code className="phix">
          {children}
        </code>
      </pre>
    }
  }
}

export default Highlighter;
```
-->

## License

Highlight.js is released under the CC0 1.0 License. See [LICENSE][1] file
for details.

### Author

Pete Lomax <petelomax@ymail.com>

### Maintainer

Pete Lomax <petelomax@ymail.com>

## Links

- The official site for the Highlight.js library is <https://highlightjs.org/>.
- The Highlight.js GitHub project: <https://github.com/highlightjs/highlight.js>
- Learn more about Phix: <http://phix.x10.mx>

[1]: https://github.com/highlightjs/highlightjs-phix/blob/master/LICENSE
