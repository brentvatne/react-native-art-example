# react-native-art-example

To use React ART on your react-native project, install react-native
`0.9.0` and then `npm i art --save`. Add `ART.xcodeproj` from
`node_modules/react-native/React/Libraries/ART` to your
Libraries and link `libART.a`. Now you can require it:

```javascript
var ReactART = require('ReactNativeART');
var {
  LinearGradient,
  RadialGradient,
  Pattern,
  Transform,
  Path,
  Surface,
  Group,
  ClippingRectangle,
  Shape,
  Text,
} = ReactART;
```

Check out `index.ios.js` to see the
[VectorWidget](https://github.com/reactjs/react-art/blob/master/examples/vector-widget/VectorWidget.js)
from [react-art](http://github.com/facebook/react-art) copied over and
running in react-native! Pictured below but not animated because licecap
was causing me some problems.

![](https://raw.githubusercontent.com/brentvatne/react-native-art-example/master/demo.png)

*Note*: This is similar to
[react-native-svg](https://www.github.com/brentvatne/react-native-svg)
but much more performant for anything that animates because it doesn't pass the entire surface
through `SVGKit` each time. You might use react-native-svg instead if
you want to load a SVG image directly and not manipulate it.
