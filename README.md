[![npm version](https://badge.fury.io/js/react-primitives-google-static-map.svg)](http://badge.fury.io/js/react-primitives-google-static-map)

# react-primitives-google-static-map

Forked from [`react-native-google-static-map`](https://github.com/yelled3/react-native-google-static-map)

A simple wrapper for an `<Image />` element with a url for Google's Static Maps:
https://developers.google.com/maps/documentation/staticmaps/intro#quick_example

Try out the API with:
http://staticmapmaker.com/google/

## Installation
```
npm install --save react-primitives-google-static-map
```
## Usage
```js
var GoogleStaticMap = require('react-primitives-google-static-map');

class MapExample extends Component {
  render() {
    return (
        <GoogleStaticMap
            style={styles.map} {...locationProps}
            latitude={'32.064171'}
            longitude={'34.7748068'}
            zoom={13}
            size={{ width: 300, height: 550 }}
        />
    );
  }
}
```
## Props
| Prop | Type | Description |
|---|---|---|
|**`latitude`**|`string`|latitude point.|
|**`longitude`**|`string`|longitude point.|
|**`size`**|`object`| the image size - `{ width: 300, height: 550 }`|
|**`zoom`**|`number`|defines the zoom level of the map.|
|**`scale`**|`number`|scale=2 returns twice as many pixels as scale=1. The default value is calculated from the screen `PixelRatio`. |
|**`format`**|`string`|'png', 'png32', 'jpg', 'gif', 'jpg-baseline'. use the `GoogleStaticMap.ImageFormats` enum. default is `png`.|
|** `markers` **| `array` | array of `{ latitude, longitude }` markers to render |
|**`mapType`**|`string`|'roadmap', 'satellite', 'terrain', 'hybrid'. use the `GoogleStaticMap.MapTypes` enum. default is `roadmap`.|
|**`hasCenterMarker`**|`bool`|add a marker on the center. default is `true`.|

and also any `Image.propTypes`.

see: http://facebook.github.io/react-primitives/docs/image.html#props

## Example
See the example in the `Example` folder.
