# number-util

The following methods are exported:

- `intBitsToFloat`
	- Returns a float for the given int bits.
- `floatToIntBits`
	- Returns int bits for the given float.
- `intToFloatColor`
	- Returns a single float representing the 
	given ABGR integer. Some precision is lost.
- `colorToFloat`
	- Returns a single float representing the
	given R, G, B, and A bytes (0 - 255). Some precision is lost.
- `isPowerOfTwo`
	- Returns true if the number is a power-of-two size
- `nextPowerOfTwo`
	- Returns the next highest power-of-two size from the given number

# example

```javascript
var util = require('number-util');

//packs the RGBA color red into a single float
var color = util.colorToFloat(255, 0, 0, 255);
```

# use

In WebGL, it's often desirable to pack RGBA data into a single float to reduce buffer upload bandwidth, at the expense of some precision loss. 

# how

Typed arrays are used to perform the casting. 