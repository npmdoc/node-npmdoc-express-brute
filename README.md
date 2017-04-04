# api documentation for  [express-brute (v1.0.1)](https://github.com/AdamPflug/express-brute#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-express-brute.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-express-brute) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-express-brute.svg)](https://travis-ci.org/npmdoc/node-npmdoc-express-brute)
#### A brute-force protection middleware for express routes that rate limits incoming requests

[![NPM](https://nodei.co/npm/express-brute.png?downloads=true)](https://www.npmjs.com/package/express-brute)

[![apidoc](https://npmdoc.github.io/node-npmdoc-express-brute/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-express-brute_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-express-brute/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-express-brute/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-express-brute/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/AdamPflug/express-brute/issues"
    },
    "dependencies": {
        "long-timeout": "~0.1.1",
        "underscore": "~1.8.3"
    },
    "description": "A brute-force protection middleware for express routes that rate limits incoming requests",
    "devDependencies": {
        "chai": "~3.5.0",
        "coveralls": "~2.11.9",
        "istanbul": "~0.4.3",
        "mocha": "~2.4.5",
        "mocha-lcov-reporter": "~1.2.0",
        "sinon": "~1.17.3",
        "sinon-chai": "~2.8.0"
    },
    "directories": {},
    "dist": {
        "shasum": "9f36d107fe34e40a682593e39bffcc53102b5335",
        "tarball": "https://registry.npmjs.org/express-brute/-/express-brute-1.0.1.tgz"
    },
    "gitHead": "ef9a73321dfe18b70b76f7acadf3f788235e3471",
    "homepage": "https://github.com/AdamPflug/express-brute#readme",
    "keywords": [
        "brute",
        "force",
        "bruteforce",
        "attack",
        "fibonacci",
        "rate",
        "limit",
        "security"
    ],
    "license": "BSD",
    "maintainers": [
        {
            "name": "adampflug",
            "email": "BluParadox@gmail.com"
        }
    ],
    "name": "express-brute",
    "optionalDependencies": {},
    "peerDependencies": {
        "express": "4.x"
    },
    "private": false,
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/AdamPflug/express-brute.git"
    },
    "scripts": {
        "test": "istanbul cover ./node_modules/mocha/bin/_mocha spec"
    },
    "version": "1.0.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module express-brute](#apidoc.module.express-brute)
1.  [function <span class="apidocSignatureSpan">express-brute.</span>AbstractClientStore ()](#apidoc.element.express-brute.AbstractClientStore)
1.  [function <span class="apidocSignatureSpan">express-brute.</span>FailForbidden (req, res, next, nextValidRequestDate)](#apidoc.element.express-brute.FailForbidden)
1.  [function <span class="apidocSignatureSpan">express-brute.</span>FailMark (req, res, next, nextValidRequestDate)](#apidoc.element.express-brute.FailMark)
1.  [function <span class="apidocSignatureSpan">express-brute.</span>FailTooManyRequests (req, res, next, nextValidRequestDate)](#apidoc.element.express-brute.FailTooManyRequests)
1.  [function <span class="apidocSignatureSpan">express-brute.</span>MemoryStore (options)](#apidoc.element.express-brute.MemoryStore)
1.  [function <span class="apidocSignatureSpan">express-brute.</span>_getKey (arr)](#apidoc.element.express-brute._getKey)
1.  number <span class="apidocSignatureSpan">express-brute.</span>instanceCount
1.  object <span class="apidocSignatureSpan">express-brute.</span>AbstractClientStore.prototype
1.  object <span class="apidocSignatureSpan">express-brute.</span>MemoryStore.prototype
1.  object <span class="apidocSignatureSpan">express-brute.</span>defaults

#### [module express-brute.AbstractClientStore](#apidoc.module.express-brute.AbstractClientStore)
1.  [function <span class="apidocSignatureSpan">express-brute.</span>AbstractClientStore ()](#apidoc.element.express-brute.AbstractClientStore.AbstractClientStore)

#### [module express-brute.AbstractClientStore.prototype](#apidoc.module.express-brute.AbstractClientStore.prototype)
1.  [function <span class="apidocSignatureSpan">express-brute.AbstractClientStore.prototype.</span>increment (key, lifetime, callback)](#apidoc.element.express-brute.AbstractClientStore.prototype.increment)

#### [module express-brute.MemoryStore](#apidoc.module.express-brute.MemoryStore)
1.  [function <span class="apidocSignatureSpan">express-brute.</span>MemoryStore (options)](#apidoc.element.express-brute.MemoryStore.MemoryStore)
1.  object <span class="apidocSignatureSpan">express-brute.MemoryStore.</span>defaults

#### [module express-brute.MemoryStore.prototype](#apidoc.module.express-brute.MemoryStore.prototype)
1.  [function <span class="apidocSignatureSpan">express-brute.MemoryStore.prototype.</span>get (key, callback)](#apidoc.element.express-brute.MemoryStore.prototype.get)
1.  [function <span class="apidocSignatureSpan">express-brute.MemoryStore.prototype.</span>reset (key, callback)](#apidoc.element.express-brute.MemoryStore.prototype.reset)
1.  [function <span class="apidocSignatureSpan">express-brute.MemoryStore.prototype.</span>set (key, value, lifetime, callback)](#apidoc.element.express-brute.MemoryStore.prototype.set)

#### [module express-brute.defaults](#apidoc.module.express-brute.defaults)
1.  boolean <span class="apidocSignatureSpan">express-brute.defaults.</span>attachResetToRequest
1.  boolean <span class="apidocSignatureSpan">express-brute.defaults.</span>refreshTimeoutOnRequest
1.  [function <span class="apidocSignatureSpan">express-brute.defaults.</span>failCallback (req, res, next, nextValidRequestDate)](#apidoc.element.express-brute.defaults.failCallback)
1.  [function <span class="apidocSignatureSpan">express-brute.defaults.</span>handleStoreError (err)](#apidoc.element.express-brute.defaults.handleStoreError)
1.  number <span class="apidocSignatureSpan">express-brute.defaults.</span>freeRetries
1.  number <span class="apidocSignatureSpan">express-brute.defaults.</span>maxWait
1.  number <span class="apidocSignatureSpan">express-brute.defaults.</span>minWait
1.  number <span class="apidocSignatureSpan">express-brute.defaults.</span>proxyDepth



# <a name="apidoc.module.express-brute"></a>[module express-brute](#apidoc.module.express-brute)

#### <a name="apidoc.element.express-brute.AbstractClientStore"></a>[function <span class="apidocSignatureSpan">express-brute.</span>AbstractClientStore ()](#apidoc.element.express-brute.AbstractClientStore)
- description and source-code
```javascript
AbstractClientStore = function () {
	
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.express-brute.FailForbidden"></a>[function <span class="apidocSignatureSpan">express-brute.</span>FailForbidden (req, res, next, nextValidRequestDate)](#apidoc.element.express-brute.FailForbidden)
- description and source-code
```javascript
FailForbidden = function (req, res, next, nextValidRequestDate) {
	setRetryAfter(res, nextValidRequestDate);
	res.status(403);
	res.send({error: {text: "Too many requests in this time frame.", nextValidRequestDate: nextValidRequestDate}});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.express-brute.FailMark"></a>[function <span class="apidocSignatureSpan">express-brute.</span>FailMark (req, res, next, nextValidRequestDate)](#apidoc.element.express-brute.FailMark)
- description and source-code
```javascript
FailMark = function (req, res, next, nextValidRequestDate) {
	res.status(429);
	setRetryAfter(res, nextValidRequestDate);
	res.nextValidRequestDate = nextValidRequestDate;
	next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.express-brute.FailTooManyRequests"></a>[function <span class="apidocSignatureSpan">express-brute.</span>FailTooManyRequests (req, res, next, nextValidRequestDate)](#apidoc.element.express-brute.FailTooManyRequests)
- description and source-code
```javascript
FailTooManyRequests = function (req, res, next, nextValidRequestDate) {
	setRetryAfter(res, nextValidRequestDate);
	res.status(429);
	res.send({error: {text: "Too many requests in this time frame.", nextValidRequestDate: nextValidRequestDate}});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.express-brute.MemoryStore"></a>[function <span class="apidocSignatureSpan">express-brute.</span>MemoryStore (options)](#apidoc.element.express-brute.MemoryStore)
- description and source-code
```javascript
MemoryStore = function (options) {
	this.data = {};
	_.bindAll(this, 'set', 'get', 'reset');
	this.options = _.extend({}, MemoryStore.defaults, options);
}
```
- example usage
```shell
...
      $ npm install express-brute

A Simple Example
----------------
''' js
var ExpressBrute = require('express-brute');

var store = new ExpressBrute.MemoryStore(); // stores state locally, don't use this in production
var bruteforce = new ExpressBrute(store);

app.post('/auth',
	bruteforce.prevent, // error 429 if we hit this route too often
	function (req, res, next) {
		res.send('Success!');
	}
...
```

#### <a name="apidoc.element.express-brute._getKey"></a>[function <span class="apidocSignatureSpan">express-brute.</span>_getKey (arr)](#apidoc.element.express-brute._getKey)
- description and source-code
```javascript
_getKey = function (arr) {
	var key = '';
	_(arr).each(function (part) {
		if (part) {
			key += crypto.createHash('sha256').update(part).digest('base64');
		}
	});
	return crypto.createHash('sha256').update(key).digest('base64');
}
```
- example usage
```shell
...
		return typeof options.failCallback === 'undefined' ? this.options.failCallback : options.failCallback;
	}, this);

	// create middleware
	return _.bind(function (req, res, next) {
		keyFunc(req, res, _.bind(function (key) {
			if(!options.ignoreIP) {
				key = ExpressBrute._getKey([req.ip, this.name, key]);
			} else {
				key = ExpressBrute._getKey([this.name, key]);
			}

			// attach a simpler "reset" function to req.brute.reset
			if (this.options.attachResetToRequest) {
				var reset = _.bind(function (callback) {
...
```



# <a name="apidoc.module.express-brute.AbstractClientStore"></a>[module express-brute.AbstractClientStore](#apidoc.module.express-brute.AbstractClientStore)

#### <a name="apidoc.element.express-brute.AbstractClientStore.AbstractClientStore"></a>[function <span class="apidocSignatureSpan">express-brute.</span>AbstractClientStore ()](#apidoc.element.express-brute.AbstractClientStore.AbstractClientStore)
- description and source-code
```javascript
AbstractClientStore = function () {
	
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.express-brute.AbstractClientStore.prototype"></a>[module express-brute.AbstractClientStore.prototype](#apidoc.module.express-brute.AbstractClientStore.prototype)

#### <a name="apidoc.element.express-brute.AbstractClientStore.prototype.increment"></a>[function <span class="apidocSignatureSpan">express-brute.AbstractClientStore.prototype.</span>increment (key, lifetime, callback)](#apidoc.element.express-brute.AbstractClientStore.prototype.increment)
- description and source-code
```javascript
increment = function (key, lifetime, callback) {
	var self = this;
	this.get(key, function (err, value) {
		if (err) {
			callback(err);
		} else {
			var count = value ? value.count+1 : 1;
			self.set(key, {count: count, lastRequest: new Date(), firstRequest: new Date()}, lifetime, function (err) {
				var prevValue = {
					count: value ? value.count : 0,
					lastRequest: value ? value.lastRequest : null,
					firstRequest: value ? value.firstRequest : null
				};
				typeof callback == 'function' && callback(err, prevValue);
			});
		}
	});
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.express-brute.MemoryStore"></a>[module express-brute.MemoryStore](#apidoc.module.express-brute.MemoryStore)

#### <a name="apidoc.element.express-brute.MemoryStore.MemoryStore"></a>[function <span class="apidocSignatureSpan">express-brute.</span>MemoryStore (options)](#apidoc.element.express-brute.MemoryStore.MemoryStore)
- description and source-code
```javascript
MemoryStore = function (options) {
	this.data = {};
	_.bindAll(this, 'set', 'get', 'reset');
	this.options = _.extend({}, MemoryStore.defaults, options);
}
```
- example usage
```shell
...
      $ npm install express-brute

A Simple Example
----------------
''' js
var ExpressBrute = require('express-brute');

var store = new ExpressBrute.MemoryStore(); // stores state locally, don't use this in production
var bruteforce = new ExpressBrute(store);

app.post('/auth',
	bruteforce.prevent, // error 429 if we hit this route too often
	function (req, res, next) {
		res.send('Success!');
	}
...
```



# <a name="apidoc.module.express-brute.MemoryStore.prototype"></a>[module express-brute.MemoryStore.prototype](#apidoc.module.express-brute.MemoryStore.prototype)

#### <a name="apidoc.element.express-brute.MemoryStore.prototype.get"></a>[function <span class="apidocSignatureSpan">express-brute.MemoryStore.prototype.</span>get (key, callback)](#apidoc.element.express-brute.MemoryStore.prototype.get)
- description and source-code
```javascript
get = function (key, callback) {
	key = this.options.prefix+key;
	var data = this.data[key] && this.data[key].value;
	if (data) {
		data = JSON.parse(data);
		data.lastRequest = new Date(data.lastRequest);
		data.firstRequest = new Date(data.firstRequest);
	}
	typeof callback == 'function' && callback(null, data);
}
```
- example usage
```shell
...
				req.brute = {
					reset: reset
				};
			}


			// filter request
			this.store.get(key, _.bind(function (err, value) {
				if (err) {
					this.options.handleStoreError({
						req: req,
						res: res,
						next: next,
						message: "Cannot get request count",
						parent: err
...
```

#### <a name="apidoc.element.express-brute.MemoryStore.prototype.reset"></a>[function <span class="apidocSignatureSpan">express-brute.MemoryStore.prototype.</span>reset (key, callback)](#apidoc.element.express-brute.MemoryStore.prototype.reset)
- description and source-code
```javascript
reset = function (key, callback) {
	key = this.options.prefix+key;
	
	if (this.data[key] && this.data[key].timeout) {
		longTimeout.clearTimeout(this.data[key].timeout);
	}
	delete this.data[key];
	typeof callback == 'function' && callback(null);
}
```
- example usage
```shell
...
			// prevent too many attempts for the same username
			next(req.body.username);
		}
	}),
	function (req, res, next) {
		if (User.isValidLogin(req.body.username, req.body.password)) { // omitted for the sake of conciseness
		 	// reset the failure counter so next time they log in they get 5 tries again before the delays kick in
			req.brute.reset(function () {
				res.redirect('/'); // logged in, send them to the home page
			});
		} else {
			res.flash('error', "Invalid username or password")
			res.redirect('/login'); // bad username/password, send them back to the login page
		}
	}
...
```

#### <a name="apidoc.element.express-brute.MemoryStore.prototype.set"></a>[function <span class="apidocSignatureSpan">express-brute.MemoryStore.prototype.</span>set (key, value, lifetime, callback)](#apidoc.element.express-brute.MemoryStore.prototype.set)
- description and source-code
```javascript
set = function (key, value, lifetime, callback) {
	key = this.options.prefix+key;
	lifetime = lifetime || 0;
	value = JSON.stringify(value);

	if (!this.data[key]) {
		this.data[key] = {};
	} else if (this.data[key].timeout) {
		longTimeout.clearTimeout(this.data[key].timeout);
	}
	this.data[key].value = value;

	if (lifetime) {
		this.data[key].timeout = longTimeout.setTimeout(_.bind(function () {
			delete this.data[key];
		}, this), 1000*lifetime);
	}
	typeof callback == 'function' && callback(null);
}
```
- example usage
```shell
...
	minWait: 25*60*60*1000, // 1 day 1 hour (should never reach this wait time)
	maxWait: 25*60*60*1000, // 1 day 1 hour (should never reach this wait time)
	lifetime: 24*60*60, // 1 day (seconds not milliseconds)
	failCallback: failCallback,
	handleStoreError: handleStoreError
});

app.set('trust proxy', 1); // Don't set to "true", it's not secure. Make sure it matches your environment
app.post('/auth',
	globalBruteforce.prevent,
	userBruteforce.getMiddleware({
		key: function(req, res, next) {
			// prevent too many attempts for the same username
			next(req.body.username);
		}
...
```



# <a name="apidoc.module.express-brute.defaults"></a>[module express-brute.defaults](#apidoc.module.express-brute.defaults)

#### <a name="apidoc.element.express-brute.defaults.failCallback"></a>[function <span class="apidocSignatureSpan">express-brute.defaults.</span>failCallback (req, res, next, nextValidRequestDate)](#apidoc.element.express-brute.defaults.failCallback)
- description and source-code
```javascript
failCallback = function (req, res, next, nextValidRequestDate) {
	setRetryAfter(res, nextValidRequestDate);
	res.status(429);
	res.send({error: {text: "Too many requests in this time frame.", nextValidRequestDate: nextValidRequestDate}});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.express-brute.defaults.handleStoreError"></a>[function <span class="apidocSignatureSpan">express-brute.defaults.</span>handleStoreError (err)](#apidoc.element.express-brute.defaults.handleStoreError)
- description and source-code
```javascript
handleStoreError = function (err) {
		throw {
			message: err.message,
			parent: err.parent
		};
	}
```
- example usage
```shell
...
				};
			}


			// filter request
			this.store.get(key, _.bind(function (err, value) {
				if (err) {
					this.options.handleStoreError({
						req: req,
						res: res,
						next: next,
						message: "Cannot get request count",
						parent: err
					});
					return;
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
