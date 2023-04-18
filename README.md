# js-crc-update
[![NPM](https://nodei.co/npm/js-crc-update.png?stars&downloads)](https://nodei.co/npm/js-crc-update/)  
Simple CRC checksum functions for JavaScript(CRC-16 and CRC-32).

## Download
[Compressed](https://github.com/Shyzuuu/js-crc-update/raw/main/crc.min.js)
[Uncompressed](https://github.com/Shyzuuu/js-crc-update/raw/main/crc.js)

## Installation
For node.js, you can use this command to install:

    npm install js-crc

## Usage
You could use like this:
```JavaScript
crc16('Message to hash');
crc32('Message to hash');
crc64('Message to hash'); // coming soon
```
If you use node.js, you should require the module first:
```JavaScript
var crc16 = require('js-crc-update').crc16;
var crc32 = require('js-crc-update').crc32;
var crc64 = require('js-crc-update').crc64; // coming soon
```
It supports AMD:
```JavaScript
require(['your/path/crc.js'], function (crc) {
    var crc16 = crc.crc16;
    var crc32 = crc.crc32;
    var crc64 = crc.crc64; // coming soon
    // ...
});

## Example
```JavaScript
crc32('The quick brown fox jumps over the lazy dog'); // 414fa339
crc32('The quick brown fox jumps over the lazy dog.'); // 519025e9

// It also supports byte `Array`, `Uint8Array`, `ArrayBuffer` input:
crc32([0]); // d202ef8d
crc32(new Uint8Array([0])); // d202ef8d
```

## License
The project is released under the [MIT license](http://www.opensource.org/licenses/MIT).
