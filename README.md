# dogecore-build

A helper to add tasks to gulp.

## Getting started

Install with:

```sh
npm install dogecore-build
```

and use and require in your gulp file: 

```javascript
var gulp = require('gulp');
var dogecoreTasks = require('dogecore-build');

dogecoreTasks('submodule');
gulp.task('default', ['lint', 'test', 'browser', 'coverage']);
```

### Notes

* There's no default task to allow for each submodule to set up their own configuration
* If the module is node-only, avoid adding the browser tasks with:
```javascript
var dogecoreTasks = require('dogecore-build');
dogecoreTasks('submodule', {skipBrowsers: true});
```


Copyright 2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.
