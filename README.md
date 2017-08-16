# React Native Exif
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors)
An image exif reader

## Installation
```sh
npm install react-native-exif --save
rnpm link react-native-exif
```

## Usage

### getExif

```javascript
import Exif from 'react-native-exif'

...

Exif.getExif('/sdcard/tt.jpg')
    .then(msg => console.warn('OK: ' + JSON.stringify(msg)))
    .catch(msg => console.warn('ERROR: ' + msg))

...

Exif.getExif('content://media/external/images/media/111')
    .then(msg => console.warn('OK: ' + JSON.stringify(msg)))
    .catch(msg => console.warn('ERROR: ' + msg))

...

Exif.getExif('assets-library://asset/asset.JPG?id=xxxx&ext=JPG')
    .then(msg => console.warn('OK: ' + JSON.stringify(msg)))
    .catch(msg => console.warn('ERROR: ' + msg))

```
#### Exif values

Value |
--- |
ImageWidth |
ImageHeight |
Orientation |
originalUri |
exif|

### getLatLong (Android only)

Fetch geo coordinates as floats.

```javascript
...
Exif.getLatLong('/sdcard/tt.jpg')
    .then(({latitude, longitude}) => {console.warn('OK: ' + latitude + ', ' + longitude)})
    .catch(msg => console.warn('ERROR: ' + msg))
...
```

Version 0.1.0 add react-native 0.40 support

## Contributors

Thanks goes to these wonderful people ([emoji key](https://github.com/kentcdodds/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
| [<img src="https://avatars3.githubusercontent.com/u/9049706?v=4" width="100px;"/><br /><sub>francisco-sanchez-molina</sub>](https://github.com/francisco-sanchez-molina)<br />[💻](https://github.com/psm1984/react-native-exif/commits?author=francisco-sanchez-molina "Code") |
| :---: |
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification. Contributions of any kind welcome!