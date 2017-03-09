# node-ocr-by-image-url
Node module based on ```node-tesseract``` to recognize texts in images by an image url.

## Install
### 1) Install the native ocr engine
```tesseract-ocr``` can be found here: [https://code.google.com/p/tesseract-ocr](https://code.google.com/p/tesseract-ocr "https://code.google.com/p/tesseract-ocr").

### 2) Install npm module
```
npm install ocr-by-image-url
```

## Usage
```js
var ocr = require('ocr-by-image-url');

ocr.getImageText('http://image.com/cat-poem.png', function(error, text){
    console.log(text.trim());
});


// With proxy
var proxy = 'http://user:pass@proxy.server.com:3128';
ocr.getImageText('http://image.com/cat.png', proxy, function(error, text){
    console.log(text.trim());
});
```
