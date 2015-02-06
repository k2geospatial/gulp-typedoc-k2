# Gulp-TypeDoc

[![NPM version](https://badge.fury.io/js/gulp-typedoc.svg)](http://badge.fury.io/js/gulp-typedoc)

[![NPM](https://nodei.co/npm/gulp-typedoc.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/gulp-typedoc/)
[![NPM](https://nodei.co/npm-dl/gulp-typedoc.png?months=9&height=3)](https://nodei.co/npm/gulp-typedoc/)

## Synopsis


Gulp plugin to execute the TypeDoc tool by Sebastian Lenz (https://sebastian-lenz.github.io/typedoc)



## Installation

You do not need to install typedoc separately, just install gulp-typedoc:

```shell
npm install --save-dev gulp-typedoc
```

## Usage

The plugin takes an object, of which all properties are passed transparently to the typedoc executable. Pipe in TypeScript files. The documentation files are not piped out, this is a future extension. 

## Code Example

```javascript

var typedoc = require("gulp-typedoc");

gulp.task("typedoc", function() {
	return gulp
		.src(["data/*.ts"])
		.pipe(typedoc({ 
			module: "commonjs", 
			out: "./out", 
			name: "my-project", 
			target: "es5"
		}))
	;
});

```

## Changelog

### 1.0.6
Moved to typedoc version 0.2.x

### 1.0.5
Moved to typedoc version 0.1.x

### 1.0.3
Use require.resolve() to find typedoc more reliably

### 1.0.2
Allow any typedoc version 0.0.x

## Contributors

* Rogier Schouten <rogier.schouten@gmail.com>
* Daan Wissing <d.wissing@spiritit.com>

## License

Apache-2.0


