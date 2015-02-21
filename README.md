# angular-uuid

angular-uuid is an AngularJS wrapper for Robert Kieffer's [node-uuid](https://github.com/broofa/node-uuid), which provides simple, fast generation of [RFC4122](http://www.ietf.org/rfc/rfc4122.txt) UUIDS.

### Features

* AngularJS service – no global scope pollution
* Generate RFC4122 version 1 or version 4 UUIDs
* Cryptographically strong random # generation on supporting platforms
* Tiny file size when minified.

### Installation

If using CommonJS then simply require angular-uuid as per usual, prior to setting up your AngularJS modules (but after including angular):

```
npm install --save angular-uuid
```

```javascript
require("angular-uuid");
```

Otherwise use a regular script tag (after including angular):

```html
<script src="angular-uuid.js"></script>
```

### Angular Module Usage

Ensure that you include *angular-uuid* in your module definition:

```javascript
var CoolApp = angular.module("CoolApp", ["angular-uuid"]);
```

You can then inject *uuid* where necessary, for example:

```javascript
CoolApp.controller("MainCtrl", ["uuid", MainCtrl]);

function MainCtrl (uuid)
{
    var hash = uuid.v4();
    console.log(hash);
}
```

### Documentation

Full documentation is available via the original project's readme: https://github.com/broofa/node-uuid/blob/master/README.md
