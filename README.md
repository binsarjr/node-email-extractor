# Node Email Extractor

[![npm](https://nodei.co/npm/node-email-extractor.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/alexa-rank-nodejs)

![npm version](https://img.shields.io/npm/v/node-email-extractor)
![lisence](https://img.shields.io/npm/l/node-email-extractor)
[![issues](https://img.shields.io/github/issues/binsarjr/node-email-extractor)](https://github.com/binsarjr/node-email-extractor/issues)
![downloads month](https://img.shields.io/npm/dm/node-email-extractor)
![downloads](https://img.shields.io/npm/dt/node-email-extractor)


Extract emails from text and also from a site page

# Includes
- [request-promise-native](https://www.npmjs.com/package/request-promise-native)

# Requirements
- [NodeJS](https://nodejs.org/en/download/)
- [npm](https://www.npmjs.com/)

# Instalation
Instalation is done using `npm install` command
```
$ npm install node-email-extractor
```

# Feutures
- Extract email from plaintext
- Extract emails from website content
- this module already supports [typescript](https://www.typescriptlang.org/)

# Usage
### javascript
```js
const email = require('node-email-extractor').default;

(async () => {
    var data = await email.url('https://www.****.com/contact-us/')
    console.log(data);
})()

var data = email.text(`Contact Details
Phone: +267 72301363 / 73316322

Email: kumindaculture@gmail.com

Registered with: `)

console.log(data)
```


### typescript
```js
import EmailExtractor from "node-email-extractor";

(async () => {
    var data = await EmailExtractor.url('https://www.****.com/contact-us/')
    console.log(data);
})()

var data = EmailExtractor.text(`Contact Details
Phone: +267 72301363 / 73316322

Email: kumindaculture@gmail.com

Registered with: `)

console.log(data)

```

### results
```js
{ domains: [ 'gmail.com' ], emails: [ 'kumindaculture@gmail.com' ] }
{ domains: [ 'gmail.com' ], emails: [ 'kumindaculture@gmail.com' ] }
```
Yes, it's really all you need to get started, Thank You ❤️