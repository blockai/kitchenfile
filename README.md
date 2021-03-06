# kitchenfile

[![Build Status](https://travis-ci.org/blockai/kitchenfile.svg?branch=master)](https://travis-ci.org/blockai/kitchenfile)

Small utility for dealing with files in tests. Only use in tests!

```javascript
import kitchenfile from 'kitchenfile'

const file = kitchenfile(`${__dirname}/files`)
// or: const file = kitchenfile(__dirname, files)

// Calls to file() are memoized!
file('image.jpg').rs() // returns a readable stream
file('image.jpg').buf // returns a buffer
file('image.jpg').path // path to image.jpg
file('image.jpg').contentType // content type based on file ext (e.g.  image/jpg)
file('image.jpg').size // file size in bytes
file('image.jpg').filename // => image.jpg
```

## Install

```bash
npm install --save-dev kitchenfile
```

Requires Node v6+

## Usage

See [./test](./test) directory for usage examples.