# helper-date [![NPM version](https://badge.fury.io/js/helper-date.svg)](http://badge.fury.io/js/helper-date)

> Format dates with date.js and moment.js. Uses date.js to parse human readable date phrases, and moment to format the rendered output. Should work with any Handlebars, Lo-Dash, underscore, or any template engine that allows helper functions to be registered. Also compatible with verb, assemble and Template.

## Examples

With Handlebars:

```handlebars
{{date "5 years ago" "YYYY"}}
//=> 2010
```

With Lo-Dash or Underscore:

```js
<%= date("5 years ago", "YYYY") %>
//=> 2010
```

With Verb (lo-dash, with special delimiters to avoid delimiter collision in markdown docs):

```js
{%= date('5 years ago', 'YYYY') %}
//=> 2010
```


## Install with [npm](npmjs.org)

```bash
npm i helper-date --save
```

## Run tests

```bash
npm test
```

## Register the helper

> This should work with any engine, here are a few examples

### [template]

Register the helper for use with any template engine

```js
template.helper('date', require('helper-date'));
```

### [assemble]

To register the helper for use with [assemble] v0.6.x:

```js
assemble.helper('date', require('helper-date'));
```

### [verb]

Register the helper for use with [verb]:

```js
var verb = require('verb');
verb.helper('date', require('helper-date'));

verb.task('default', function() {
  verb.src('.verb*.md')
    .pipe(verb.dest('./'));
});
```

### [handlebars]

```js
var handlebars = require('handlebars');
handlebars.registerHelper('date', require('helper-date'));
```
Usage

```handlebars
{{date "5 years ago" "YYYY"}}
```

### [Lo-Dash] or [underscore]

```js
// as a mixin
_.mixin({date: dateHelper});
_.template('<%= _.date("5 years ago", "YYYY") %>', {});
//=> 2010

// passed on the context
_.template('<%= date("5 years ago", "YYYY") %>', {date: dateHelper});
//=> 2010

// as an import
var settings = {imports: {date: dateHelper}};
_.template('<%= date("5 years ago", "YYYY") %>', {}, settings);
//=> 2010
```

## Contributing
Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/helpers/helper-date/issues)

To request or contribute a helper to the [github.com/helpers][helpers] org, please read [this contributing guide][guide] to get started.

## Author

**Jon Schlinkert**
 
+ [github/helpers](https://github.com/helpers)
+ [twitter/helpers](http://twitter.com/helpers) 

## License
Copyright (c) 2015 Jon Schlinkert  
Released under the MIT license

***

_This file was generated by [verb](https://github.com/assemble/verb) on February 17, 2015._

[assemble]: https://github.com/assemble/assemble
[generator-verb]: https://github.com/assemble/generator-verb
[handlebars-helpers]: https://github.com/assemble/handlebars-helpers/
[handlebars]: https://github.com/wycats/handlebars.js/
[helpers]: https://github.com/helpers
[Lo-Dash]: https://lodash.com/
[template]: https://github.com/jonschlinkert/template
[underscore]: https://github.com/jashkenas/underscore
[verb]: https://github.com/assemble/verb
[guide]: https://github.com/helpers/requests