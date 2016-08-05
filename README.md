# Savor

<p align="center">
  <a href="https://github.com/idancali/savor">
    <img height="256" src="https://raw.githubusercontent.com/idancali/savor/master/logo.png">
  </a>
  <p align="center"> <b> Savor </b> Adds Delicious Flavors To Your Node Module, Like Tests, Coverage and Analysis. </p>
</p>

[![Version](https://img.shields.io/npm/v/savor.svg)](https://www.npmjs.com/package/savor)
[![Build Status](https://travis-ci.org/idancali/savor.svg?branch=master)](https://travis-ci.org/idancali/savor)

# Installation

**STEP 1**

Add Savor to your module as a development dependency:

```javascript
npm install --save-dev savor
```

**STEP 2**

Add Savor to your module scripts:

```javascript
"scripts": {
  "savor": "./node_modules/.bin/savor"
}
```

If you'd like more granularity over your scripts you can also install single Savor commands:

```javascript
"scripts": {
  "savor": "./node_modules/.bin/savor",
  "test": "./node_modules/.bin/savor test",
  "lint": "./node_modules/.bin/savor lint",
  "cover": "./node_modules/.bin/savor cover",
  "coveralls": "./node_modules/.bin/savor coveralls",
  "codacy": "./node_modules/.bin/savor codacy"
}
```

**STEP 3**

Make sure your code resides under a ```src``` directory and all your tests under a ```test``` directory, like so:

```javascript
package.json
node_modules/
src/
test/
```

# Adding Tests

You can now write tests under your ```test``` directory, like so:

```javascript
var savor = require('savor');

savor.add('this is a test', function(done, context) {
  console.log('My test is running');

  // The test finished successfully
  done && done();

  // Or throw an error if the test fails
  // done && done(new Error('ddd'));
}).

// You can keep adding tests here with savor.add

run();
```

# Running Tests

You can now simply run your tests like so:

```javascript
npm test
```

or like this:

```javascript
npm run test
```

or even like this:

```javascript
npm run savor test
```

# Test coverage

You can check your coverage like this:

```javascript
npm run coverage
```

or like this:

```javascript
npm run savor coverage
```

# Static analysis

You can lint your code like this:

```javascript
npm run lint
```

or like this:

```javascript
npm run savor lint
```

# License

Copyright (c) 2016 I. Dan Calinescu

 Licensed under the The MIT License (MIT) (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at

 https://raw.githubusercontent.com/idancali/savor/master/LICENSE

 Unless required by applicable law or agreed to in writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
