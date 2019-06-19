<div align="center">
	<br>
  	<p>
		<a href="https://krunker.io"><img src="https://i.imgur.com/qvTc8OA.png" width="546" alt="Krunker.js"></a>
  	</p>
  	<br>
  	<p>
		<a href="https://www.npmjs.com/package/krunker.js">
			<img src="https://yt3.ggpht.com/-PXH7hCkUVLA/AAAAAAAAAAI/AAAAAAAAAAc/oDSLu0ZELm8/s88-mo-c-c0xffffffff-rj-k-no/photo.jpg?maxAge=3600" alt="NPM version">
		</a>
		<a href="https://youtu.be/JYuoJ2Zm0LY">
			<img src="https://yt3.ggpht.com/-PXH7hCkUVLA/AAAAAAAAAAI/AAAAAAAAAAc/oDSLu0ZELm8/s88-mo-c-c0xffffffff-rj-k-no/photo.jpg?maxAge=3600" alt="NPM downloads">
		</a>
		<a href="https://youtu.be/JYuoJ2Zm0LY">
			<img src="https://yt3.ggpht.com/-PXH7hCkUVLA/AAAAAAAAAAI/AAAAAAAAAAc/oDSLu0ZELm8/s88-mo-c-c0xffffffff-rj-k-no/photo.jpg?maxAge=3600" alt="Dependencies">
		</a>
		<a href="https://youtu.be/JYuoJ2Zm0LY">
			<img src="https://yt3.ggpht.com/-PXH7hCkUVLA/AAAAAAAAAAI/AAAAAAAAAAc/oDSLu0ZELm8/s88-mo-c-c0xffffffff-rj-k-no/photo.jpg" alt="Build status">
		</a>
	</p>
  	<p>
		<a href="https://youtu.be/JYuoJ2Zm0LY/">
			<img src="https://yt3.ggpht.com/-PXH7hCkUVLA/AAAAAAAAAAI/AAAAAAAAAAc/oDSLu0ZELm8/s88-mo-c-c0xffffffff-rj-k-no/photo.jpg?downloads=true&stars=true" alt="npm installnfo">
		</a>
  	</p>
</div>

###### [GitHub](https://github.com/xAzz) | [Discord](https://discord.gg/wB3P92h)

A simple, easy to use module for interacting with the [Krunker.io Social Page](https://krunker.io/social.html)

## Setup and Installation

```
$ npm i krunker.js
```

## [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)-based Example Usage

```js
// Require the NPM Module
const KrunkerJS = require('krunker.js');
// Create a new instance
const Krunker = new KrunkerJS();

// Get the stats of the user
Krunker.getUser('Helinho').then(data => {
	// Console log the user stats as an object
	console.log(data);
	// [V1.2^ Feature] Gets all stats ready as an object
	console.log(data.simplified);

	// Convert Player Score to Level
	Krunker.getLevel(data);
	// Convert Time Played
	Krunker.getPlayTime(data);
	// Get user KDR
	Krunker.getKDR(data);
	// Get W/L
	Krunker.getWL(data);
	// Get SPK
	Krunker.getSPK(data);
}).catch(console.error);
```

## [async](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)/await-Based Example

```js
// Require the NPM Module
const KrunkerJS = require('krunker.js');
// Create a new instance
const Krunker = new KrunkerJS();

(async () => {
	try {
		// Get the stats of the user
		const user = await Krunker.getUser('Helinho');
		// Console log the user stats as an object
		console.log(user);
		// [V1.2^ Feature] Gets all stats ready as an object
		console.log(user.simplified);
	} catch (e) {
		console.error(e);
	}
})();
```

## Help

If you don't understand something in the documentation, you are experiencing problems, or you just need a gentle
nudge in the right direction, please don't hesitate to join my [Development Server](https://discord.gg/TpGPFXg).
