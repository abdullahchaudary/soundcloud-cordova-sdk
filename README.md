SoundCloud Cordova SDK
======================

Unfortunately since the SoundCloud JavaScript SDK uses protocol-relative URLs in its requests to the SoundCloud API, the SDK doesn't work when running on an Android or iOS device under Cordova, as the URLs will resolve the the `file://` protocol.

As this issue [has not been addressed](https://github.com/soundcloud/soundcloud-javascript/issues/16) by SoundCloud, this repository contains an inelegantly patched version of the minified distribution of the SDK.

Usage
-----

Install the SDK via npm:

```
npm install --save soundcloud-cordova-sdk
```

Import the SDK into your application:

```js
import 'soundcloud-cordova-sdk';

// Initialize the SDK with your SoundCloud Client ID
SC.initialize({
  client_id: 'CLIENT_ID',
});
```
