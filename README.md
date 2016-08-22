# structured-log-seq-sink [![Build Status](https://travis-ci.org/Wedvich/structured-log-seq-sink.svg?branch=master)](https://travis-ci.org/Wedvich/structured-log-seq-sink) [![npm version](https://badge.fury.io/js/structured-log-seq-sink.svg)](https://www.npmjs.com/package/structured-log-seq-sink)

A [structured-log](https://github.com/structured-log/structured-log) plugin that writes log events to Seq.

Uses [es6-promise](https://github.com/stefanpenner/es6-promise) and [isomorphic-fetch](https://github.com/matthew-andrews/isomorphic-fetch) to polyfill Promises and fetch, respectively.

### Installing

`npm i structured-log-seq-sink --save`

### Using

```
var structuredLog = require('structured-log');
var seqSink = require('structured-log-seq-sink');

var logger = structuredLog.configure()
  .writeTo(seqSink({ /* options */ }))
  .create();

```

##### Available options

- `apiKey` API key to use
- `url` (required) The URL to the Seq server

### Building

To build the modules, ensure [Rollup](http://rollupjs.org/) is installed globally, and run the `build` script:

```
npm i rollup -g
npm run build
```

### Testing

```
npm test
```
