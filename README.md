# api documentation for  [redux-api-middleware (v1.0.2)](https://github.com/agraboso/redux-api-middleware)  [![npm package](https://img.shields.io/npm/v/npmdoc-redux-api-middleware.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-redux-api-middleware) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-redux-api-middleware.svg)](https://travis-ci.org/npmdoc/node-npmdoc-redux-api-middleware)
#### Redux middleware for calling an API.

[![NPM](https://nodei.co/npm/redux-api-middleware.png?downloads=true)](https://www.npmjs.com/package/redux-api-middleware)

[![apidoc](https://npmdoc.github.io/node-npmdoc-redux-api-middleware/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-redux-api-middleware_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-redux-api-middleware/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-redux-api-middleware/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-redux-api-middleware/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Alberto Garcia-Raboso",
        "email": "agraboso@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/agraboso/redux-api-middleware/issues"
    },
    "dependencies": {
        "babel-runtime": "^5.8.25",
        "isomorphic-fetch": "^2.1.1",
        "lodash.isplainobject": "^3.2.0"
    },
    "description": "Redux middleware for calling an API.",
    "devDependencies": {
        "babel": "^5.8.23",
        "babel-eslint": "^4.1.3",
        "babel-istanbul": "^0.3.20",
        "coveralls": "^2.11.4",
        "eslint": "^1.6.0",
        "eslint-plugin-babel": "^2.1.1",
        "nock": "^2.15.0",
        "normalizr": "^1.1.0",
        "rimraf": "^2.4.3",
        "tap-spec": "^4.1.0",
        "tape": "^4.2.1"
    },
    "directories": {},
    "dist": {
        "shasum": "77a82ce6ef98359c7025679ca752470bd90576c0",
        "tarball": "https://registry.npmjs.org/redux-api-middleware/-/redux-api-middleware-1.0.2.tgz"
    },
    "files": [
        "README.md",
        "LICENSE.md",
        "lib/"
    ],
    "gitHead": "e72ac27801cab4f5c5cedfaa8d1787e0ffce6f5b",
    "homepage": "https://github.com/agraboso/redux-api-middleware",
    "keywords": [
        "redux",
        "api",
        "middleware",
        "redux-middleware",
        "flux"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "agraboso",
            "email": "agraboso@gmail.com"
        }
    ],
    "name": "redux-api-middleware",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/agraboso/redux-api-middleware.git"
    },
    "scripts": {
        "build": "babel src --out-dir lib",
        "clean": "rimraf lib coverage",
        "cover": "babel-node ./node_modules/.bin/babel-istanbul cover test/index.js | tap-spec",
        "lint": "eslint src test",
        "prepublish": "npm run lint && npm test && npm run clean && npm run build",
        "test": "babel-node test/index.js | tap-spec"
    },
    "version": "1.0.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module redux-api-middleware](#apidoc.module.redux-api-middleware)
1.  boolean <span class="apidocSignatureSpan">redux-api-middleware.</span>__esModule
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.</span>ApiError (status, statusText, response)](#apidoc.element.redux-api-middleware.ApiError)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.</span>InternalError (message)](#apidoc.element.redux-api-middleware.InternalError)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.</span>InvalidRSAA (validationErrors)](#apidoc.element.redux-api-middleware.InvalidRSAA)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.</span>RequestError (message)](#apidoc.element.redux-api-middleware.RequestError)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.</span>apiMiddleware (_ref)](#apidoc.element.redux-api-middleware.apiMiddleware)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.</span>getJSON (res)](#apidoc.element.redux-api-middleware.getJSON)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.</span>isRSAA (action)](#apidoc.element.redux-api-middleware.isRSAA)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.</span>isValidRSAA (action)](#apidoc.element.redux-api-middleware.isValidRSAA)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.</span>validateRSAA (action)](#apidoc.element.redux-api-middleware.validateRSAA)
1.  object <span class="apidocSignatureSpan">redux-api-middleware.</span>errors
1.  object <span class="apidocSignatureSpan">redux-api-middleware.</span>middleware
1.  object <span class="apidocSignatureSpan">redux-api-middleware.</span>util
1.  object <span class="apidocSignatureSpan">redux-api-middleware.</span>validation
1.  symbol <span class="apidocSignatureSpan">redux-api-middleware.</span>CALL_API

#### [module redux-api-middleware.errors](#apidoc.module.redux-api-middleware.errors)
1.  boolean <span class="apidocSignatureSpan">redux-api-middleware.errors.</span>__esModule
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.errors.</span>ApiError (status, statusText, response)](#apidoc.element.redux-api-middleware.errors.ApiError)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.errors.</span>InternalError (message)](#apidoc.element.redux-api-middleware.errors.InternalError)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.errors.</span>InvalidRSAA (validationErrors)](#apidoc.element.redux-api-middleware.errors.InvalidRSAA)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.errors.</span>RequestError (message)](#apidoc.element.redux-api-middleware.errors.RequestError)

#### [module redux-api-middleware.middleware](#apidoc.module.redux-api-middleware.middleware)
1.  boolean <span class="apidocSignatureSpan">redux-api-middleware.middleware.</span>__esModule
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.middleware.</span>apiMiddleware (_ref)](#apidoc.element.redux-api-middleware.middleware.apiMiddleware)

#### [module redux-api-middleware.util](#apidoc.module.redux-api-middleware.util)
1.  boolean <span class="apidocSignatureSpan">redux-api-middleware.util.</span>__esModule
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.util.</span>actionWith (descriptor, args)](#apidoc.element.redux-api-middleware.util.actionWith)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.util.</span>getJSON (res)](#apidoc.element.redux-api-middleware.util.getJSON)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.util.</span>normalizeTypeDescriptors (types)](#apidoc.element.redux-api-middleware.util.normalizeTypeDescriptors)

#### [module redux-api-middleware.validation](#apidoc.module.redux-api-middleware.validation)
1.  boolean <span class="apidocSignatureSpan">redux-api-middleware.validation.</span>__esModule
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.validation.</span>isRSAA (action)](#apidoc.element.redux-api-middleware.validation.isRSAA)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.validation.</span>isValidRSAA (action)](#apidoc.element.redux-api-middleware.validation.isValidRSAA)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.validation.</span>isValidTypeDescriptor (obj)](#apidoc.element.redux-api-middleware.validation.isValidTypeDescriptor)
1.  [function <span class="apidocSignatureSpan">redux-api-middleware.validation.</span>validateRSAA (action)](#apidoc.element.redux-api-middleware.validation.validateRSAA)



# <a name="apidoc.module.redux-api-middleware"></a>[module redux-api-middleware](#apidoc.module.redux-api-middleware)

#### <a name="apidoc.element.redux-api-middleware.ApiError"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.</span>ApiError (status, statusText, response)](#apidoc.element.redux-api-middleware.ApiError)
- description and source-code
```javascript
function ApiError(status, statusText, response) {
  _classCallCheck(this, ApiError);

  _Error4.call(this);
  this.name = 'ApiError';
  this.status = status;
  this.statusText = statusText;
  this.response = response;
  this.message = status + ' - ' + statusText;
}
```
- example usage
```shell
...

  if (typeof failureType === 'string' || typeof failureType === 'symbol') {
    failureType = { type: failureType };
  }
  failureType = _extends({
    payload: function payload(action, state, res) {
      return getJSON(res).then(function (json) {
        return new _errors.ApiError(res.status, res.statusText, json);
      });
    }
  }, failureType);

  return [requestType, successType, failureType];
}
...
```

#### <a name="apidoc.element.redux-api-middleware.InternalError"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.</span>InternalError (message)](#apidoc.element.redux-api-middleware.InternalError)
- description and source-code
```javascript
function InternalError(message) {
  _classCallCheck(this, InternalError);

  _Error2.call(this);
  this.name = 'InternalError';
  this.message = message;
}
```
- example usage
```shell
...
  context$1$0.next = 10;
  break;

case 6:
  context$1$0.prev = 6;
  context$1$0.t0 = context$1$0['catch'](0);

  descriptor.payload = new _errors.InternalError(context$1$0.t0.message);
  descriptor.error = true;

case 10:
  context$1$0.prev = 10;
  context$1$0.next = 13;
  return _regeneratorRuntime.awrap(typeof descriptor.meta === 'function' ? descriptor.meta.apply(descriptor, args) : descriptor.
meta);
...
```

#### <a name="apidoc.element.redux-api-middleware.InvalidRSAA"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.</span>InvalidRSAA (validationErrors)](#apidoc.element.redux-api-middleware.InvalidRSAA)
- description and source-code
```javascript
function InvalidRSAA(validationErrors) {
  _classCallCheck(this, InvalidRSAA);

  _Error.call(this);
  this.name = 'InvalidRSAA';
  this.message = 'Invalid RSAA';
  this.validationErrors = validationErrors;
}
```
- example usage
```shell
...
    _requestType = _callAPI.types[0];

    if (_requestType && _requestType.type) {
      _requestType = _requestType.type;
    }
    next({
      type: _requestType,
      payload: new _errors.InvalidRSAA(validationErrors),
      error: true
    });
  }
  return context$3$0.abrupt('return');

case 7:
  callAPI = action[_CALL_API2['default']];
...
```

#### <a name="apidoc.element.redux-api-middleware.RequestError"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.</span>RequestError (message)](#apidoc.element.redux-api-middleware.RequestError)
- description and source-code
```javascript
function RequestError(message) {
  _classCallCheck(this, RequestError);

  _Error3.call(this);
  this.name = 'RequestError';
  this.message = message;
}
```
- example usage
```shell
...
  break;

case 24:
  context$3$0.prev = 24;
  context$3$0.t0 = context$3$0['catch'](19);
  context$3$0.next = 28;
  return _regeneratorRuntime.awrap(_util.actionWith(_extends({}, requestType, {
    payload: new _errors.RequestError('[CALL_API].bailout function failed'),
    error: true
  }), [action, getState()]));

case 28:
  context$3$0.t1 = context$3$0.sent;
  return context$3$0.abrupt('return', next(context$3$0.t1));
...
```

#### <a name="apidoc.element.redux-api-middleware.apiMiddleware"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.</span>apiMiddleware (_ref)](#apidoc.element.redux-api-middleware.apiMiddleware)
- description and source-code
```javascript
function apiMiddleware(_ref) {
  var _this = this;

  var getState = _ref.getState;

  return function (next) {
    return function callee$2$0(action) {
      var validationErrors, _callAPI, _requestType, callAPI, endpoint, headers, method, body, credentials, bailout, types, _normalizeTypeDescriptors
, requestType, successType, failureType, res;

      return _regeneratorRuntime.async(function callee$2$0$(context$3$0) {
        while (1) switch (context$3$0.prev = context$3$0.next) {
          case 0:
            if (_validation.isRSAA(action)) {
              context$3$0.next = 2;
              break;
            }

            return context$3$0.abrupt('return', next(action));

          case 2:
            validationErrors = _validation.validateRSAA(action);

            if (!validationErrors.length) {
              context$3$0.next = 7;
              break;
            }

            _callAPI = action[_CALL_API2['default']];

            if (_callAPI.types && Array.isArray(_callAPI.types)) {
              _requestType = _callAPI.types[0];

              if (_requestType && _requestType.type) {
                _requestType = _requestType.type;
              }
              next({
                type: _requestType,
                payload: new _errors.InvalidRSAA(validationErrors),
                error: true
              });
            }
            return context$3$0.abrupt('return');

          case 7:
            callAPI = action[_CALL_API2['default']];
            endpoint = callAPI.endpoint;
            headers = callAPI.headers;
            method = callAPI.method;
            body = callAPI.body;
            credentials = callAPI.credentials;
            bailout = callAPI.bailout;
            types = callAPI.types;
            _normalizeTypeDescriptors = _util.normalizeTypeDescriptors(types);
            requestType = _normalizeTypeDescriptors[0];
            successType = _normalizeTypeDescriptors[1];
            failureType = _normalizeTypeDescriptors[2];
            context$3$0.prev = 19;

            if (!(typeof bailout === 'boolean' && bailout || typeof bailout === 'function' && bailout(getState()))) {
              context$3$0.next = 22;
              break;
            }

            return context$3$0.abrupt('return');

          case 22:
            context$3$0.next = 30;
            break;

          case 24:
            context$3$0.prev = 24;
            context$3$0.t0 = context$3$0['catch'](19);
            context$3$0.next = 28;
            return _regeneratorRuntime.awrap(_util.actionWith(_extends({}, requestType, {
              payload: new _errors.RequestError('[CALL_API].bailout function failed'),
              error: true
            }), [action, getState()]));

          case 28:
            context$3$0.t1 = context$3$0.sent;
            return context$3$0.abrupt('return', next(context$3$0.t1));

          case 30:
            if (!(typeof endpoint === 'function')) {
              context$3$0.next = 41;
              break;
            }

            context$3$0.prev = 31;

            endpoint = endpoint(getState());
            context$3$0.next = 41;
            break;

          case 35:
            context$3$0.prev = 35;
            context$3$0.t2 = context$3$0['catch'](31);
            context$3$0.next = 39;
            return _regeneratorRuntime.awrap(_util.actionWith(_extends({}, requestType, {
              payload: new _errors.RequestError('[CALL_API].endpoint function failed'),
              error: true
            }), [action, getState()]));

          case 39:
            context$3$0.t3 = context$3$0.sent;
            return context$3$0.abrupt('return', next(context$3$0.t3));

          case 41:
            if (!(typeof headers === 'function')) {
              context$3$0.next = 52;
              break;
            }

            context$3$0.prev = 42;

            headers = headers(getState());
            context$3$0.next = 52;
            break;

          case 46:
            context$3$0.prev = 46;
            context$3$0.t4 = context$3$0['catch'](42);
            context ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-api-middleware.getJSON"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.</span>getJSON (res)](#apidoc.element.redux-api-middleware.getJSON)
- description and source-code
```javascript
function getJSON(res) {
  var contentType, emptyCodes;
  return _regeneratorRuntime.async(function getJSON$(context$1$0) {
    while (1) switch (context$1$0.prev = context$1$0.next) {
      case 0:
        contentType = res.headers.get('Content-Type');
        emptyCodes = [204, 205];

        if (!(! ~emptyCodes.indexOf(res.status) && contentType && ~contentType.indexOf('json'))) {
          context$1$0.next = 8;
          break;
        }

        context$1$0.next = 5;
        return _regeneratorRuntime.awrap(res.json());

      case 5:
        return context$1$0.abrupt('return', context$1$0.sent);

      case 8:
        context$1$0.next = 10;
        return _regeneratorRuntime.awrap(_Promise.resolve());

      case 10:
        return context$1$0.abrupt('return', context$1$0.sent);

      case 11:
      case 'end':
        return context$1$0.stop();
    }
  }, null, this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-api-middleware.isRSAA"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.</span>isRSAA (action)](#apidoc.element.redux-api-middleware.isRSAA)
- description and source-code
```javascript
function isRSAA(action) {
  return _lodashIsplainobject2['default'](action) && action.hasOwnProperty(_CALL_API2['default']);
}
```
- example usage
```shell
...
  return function (next) {
    return function callee$2$0(action) {
      var validationErrors, _callAPI, _requestType, callAPI, endpoint, headers, method, body, credentials, bailout, types, _normalizeTypeDescriptors
, requestType, successType, failureType, res;

      return _regeneratorRuntime.async(function callee$2$0$(context$3$0) {
        while (1) switch (context$3$0.prev = context$3$0.next) {
case 0:
  if (_validation.isRSAA(action)) {
    context$3$0.next = 2;
    break;
  }

  return context$3$0.abrupt('return', next(action));

case 2:
...
```

#### <a name="apidoc.element.redux-api-middleware.isValidRSAA"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.</span>isValidRSAA (action)](#apidoc.element.redux-api-middleware.isValidRSAA)
- description and source-code
```javascript
function isValidRSAA(action) {
  return !validateRSAA(action).length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-api-middleware.validateRSAA"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.</span>validateRSAA (action)](#apidoc.element.redux-api-middleware.validateRSAA)
- description and source-code
```javascript
function validateRSAA(action) {
  var validationErrors = [];
  var validCallAPIKeys = ['endpoint', 'method', 'body', 'headers', 'credentials', 'bailout', 'types'];
  var validMethods = ['GET', 'HEAD', 'POST', 'PUT', 'PATCH', 'DELETE', 'OPTIONS'];
  var validCredentials = ['omit', 'same-origin', 'include'];

  if (!isRSAA(action)) {
    validationErrors.push('RSAAs must be plain JavaScript objects with a [CALL_API] property');
    return validationErrors;
  }

  for (var key in action) {
    if (key !== [_CALL_API2['default']]) {
      validationErrors.push('Invalid root key: ' + key);
    }
  }

  var callAPI = action[_CALL_API2['default']];
  if (!_lodashIsplainobject2['default'](callAPI)) {
    validationErrors.push('[CALL_API] property must be a plain JavaScript object');
  }
  for (var key in callAPI) {
    if (! ~validCallAPIKeys.indexOf(key)) {
      validationErrors.push('Invalid [CALL_API] key: ' + key);
    }
  }

  var endpoint = callAPI.endpoint;
  var method = callAPI.method;
  var headers = callAPI.headers;
  var credentials = callAPI.credentials;
  var types = callAPI.types;
  var bailout = callAPI.bailout;

  if (typeof endpoint === 'undefined') {
    validationErrors.push('[CALL_API] must have an endpoint property');
  } else if (typeof endpoint !== 'string' && typeof endpoint !== 'function') {
    validationErrors.push('[CALL_API].endpoint property must be a string or a function');
  }
  if (typeof method === 'undefined') {
    validationErrors.push('[CALL_API] must have a method property');
  } else if (typeof method !== 'string') {
    validationErrors.push('[CALL_API].method property must be a string');
  } else if (! ~validMethods.indexOf(method.toUpperCase())) {
    validationErrors.push('Invalid [CALL_API].method: ' + method.toUpperCase());
  }

  if (typeof headers !== 'undefined' && !_lodashIsplainobject2['default'](headers) && typeof headers !== 'function') {
    validationErrors.push('[CALL_API].headers property must be undefined, a plain JavaScript object, or a function');
  }
  if (typeof credentials !== 'undefined') {
    if (typeof credentials !== 'string') {
      validationErrors.push('[CALL_API].credentials property must be undefined, or a string');
    } else if (! ~validCredentials.indexOf(credentials)) {
      validationErrors.push('Invalid [CALL_API].credentials: ' + credentials);
    }
  }
  if (typeof bailout !== 'undefined' && typeof bailout !== 'boolean' && typeof bailout !== 'function') {
    validationErrors.push('[CALL_API].bailout property must be undefined, a boolean, or a function');
  }

  if (typeof types === 'undefined') {
    validationErrors.push('[CALL_API] must have a types property');
  } else if (!Array.isArray(types) || types.length !== 3) {
    validationErrors.push('[CALL_API].types property must be an array of length 3');
  } else {
    var requestType = types[0];
    var successType = types[1];
    var failureType = types[2];

    if (typeof requestType !== 'string' && typeof requestType !== 'symbol' && !isValidTypeDescriptor(requestType)) {
      validationErrors.push('Invalid request type');
    }
    if (typeof successType !== 'string' && typeof successType !== 'symbol' && !isValidTypeDescriptor(successType)) {
      validationErrors.push('Invalid success type');
    }
    if (typeof failureType !== 'string' && typeof failureType !== 'symbol' && !isValidTypeDescriptor(failureType)) {
      validationErrors.push('Invalid failure type');
    }
  }

  return validationErrors;
}
```
- example usage
```shell
...
  context$3$0.next = 2;
  break;
}

return context$3$0.abrupt('return', next(action));

          case 2:
validationErrors = _validation.validateRSAA(action);

if (!validationErrors.length) {
  context$3$0.next = 7;
  break;
}

_callAPI = action[_CALL_API2['default']];
...
```



# <a name="apidoc.module.redux-api-middleware.errors"></a>[module redux-api-middleware.errors](#apidoc.module.redux-api-middleware.errors)

#### <a name="apidoc.element.redux-api-middleware.errors.ApiError"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.errors.</span>ApiError (status, statusText, response)](#apidoc.element.redux-api-middleware.errors.ApiError)
- description and source-code
```javascript
function ApiError(status, statusText, response) {
  _classCallCheck(this, ApiError);

  _Error4.call(this);
  this.name = 'ApiError';
  this.status = status;
  this.statusText = statusText;
  this.response = response;
  this.message = status + ' - ' + statusText;
}
```
- example usage
```shell
...

  if (typeof failureType === 'string' || typeof failureType === 'symbol') {
    failureType = { type: failureType };
  }
  failureType = _extends({
    payload: function payload(action, state, res) {
      return getJSON(res).then(function (json) {
        return new _errors.ApiError(res.status, res.statusText, json);
      });
    }
  }, failureType);

  return [requestType, successType, failureType];
}
...
```

#### <a name="apidoc.element.redux-api-middleware.errors.InternalError"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.errors.</span>InternalError (message)](#apidoc.element.redux-api-middleware.errors.InternalError)
- description and source-code
```javascript
function InternalError(message) {
  _classCallCheck(this, InternalError);

  _Error2.call(this);
  this.name = 'InternalError';
  this.message = message;
}
```
- example usage
```shell
...
  context$1$0.next = 10;
  break;

case 6:
  context$1$0.prev = 6;
  context$1$0.t0 = context$1$0['catch'](0);

  descriptor.payload = new _errors.InternalError(context$1$0.t0.message);
  descriptor.error = true;

case 10:
  context$1$0.prev = 10;
  context$1$0.next = 13;
  return _regeneratorRuntime.awrap(typeof descriptor.meta === 'function' ? descriptor.meta.apply(descriptor, args) : descriptor.
meta);
...
```

#### <a name="apidoc.element.redux-api-middleware.errors.InvalidRSAA"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.errors.</span>InvalidRSAA (validationErrors)](#apidoc.element.redux-api-middleware.errors.InvalidRSAA)
- description and source-code
```javascript
function InvalidRSAA(validationErrors) {
  _classCallCheck(this, InvalidRSAA);

  _Error.call(this);
  this.name = 'InvalidRSAA';
  this.message = 'Invalid RSAA';
  this.validationErrors = validationErrors;
}
```
- example usage
```shell
...
    _requestType = _callAPI.types[0];

    if (_requestType && _requestType.type) {
      _requestType = _requestType.type;
    }
    next({
      type: _requestType,
      payload: new _errors.InvalidRSAA(validationErrors),
      error: true
    });
  }
  return context$3$0.abrupt('return');

case 7:
  callAPI = action[_CALL_API2['default']];
...
```

#### <a name="apidoc.element.redux-api-middleware.errors.RequestError"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.errors.</span>RequestError (message)](#apidoc.element.redux-api-middleware.errors.RequestError)
- description and source-code
```javascript
function RequestError(message) {
  _classCallCheck(this, RequestError);

  _Error3.call(this);
  this.name = 'RequestError';
  this.message = message;
}
```
- example usage
```shell
...
  break;

case 24:
  context$3$0.prev = 24;
  context$3$0.t0 = context$3$0['catch'](19);
  context$3$0.next = 28;
  return _regeneratorRuntime.awrap(_util.actionWith(_extends({}, requestType, {
    payload: new _errors.RequestError('[CALL_API].bailout function failed'),
    error: true
  }), [action, getState()]));

case 28:
  context$3$0.t1 = context$3$0.sent;
  return context$3$0.abrupt('return', next(context$3$0.t1));
...
```



# <a name="apidoc.module.redux-api-middleware.middleware"></a>[module redux-api-middleware.middleware](#apidoc.module.redux-api-middleware.middleware)

#### <a name="apidoc.element.redux-api-middleware.middleware.apiMiddleware"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.middleware.</span>apiMiddleware (_ref)](#apidoc.element.redux-api-middleware.middleware.apiMiddleware)
- description and source-code
```javascript
function apiMiddleware(_ref) {
  var _this = this;

  var getState = _ref.getState;

  return function (next) {
    return function callee$2$0(action) {
      var validationErrors, _callAPI, _requestType, callAPI, endpoint, headers, method, body, credentials, bailout, types, _normalizeTypeDescriptors
, requestType, successType, failureType, res;

      return _regeneratorRuntime.async(function callee$2$0$(context$3$0) {
        while (1) switch (context$3$0.prev = context$3$0.next) {
          case 0:
            if (_validation.isRSAA(action)) {
              context$3$0.next = 2;
              break;
            }

            return context$3$0.abrupt('return', next(action));

          case 2:
            validationErrors = _validation.validateRSAA(action);

            if (!validationErrors.length) {
              context$3$0.next = 7;
              break;
            }

            _callAPI = action[_CALL_API2['default']];

            if (_callAPI.types && Array.isArray(_callAPI.types)) {
              _requestType = _callAPI.types[0];

              if (_requestType && _requestType.type) {
                _requestType = _requestType.type;
              }
              next({
                type: _requestType,
                payload: new _errors.InvalidRSAA(validationErrors),
                error: true
              });
            }
            return context$3$0.abrupt('return');

          case 7:
            callAPI = action[_CALL_API2['default']];
            endpoint = callAPI.endpoint;
            headers = callAPI.headers;
            method = callAPI.method;
            body = callAPI.body;
            credentials = callAPI.credentials;
            bailout = callAPI.bailout;
            types = callAPI.types;
            _normalizeTypeDescriptors = _util.normalizeTypeDescriptors(types);
            requestType = _normalizeTypeDescriptors[0];
            successType = _normalizeTypeDescriptors[1];
            failureType = _normalizeTypeDescriptors[2];
            context$3$0.prev = 19;

            if (!(typeof bailout === 'boolean' && bailout || typeof bailout === 'function' && bailout(getState()))) {
              context$3$0.next = 22;
              break;
            }

            return context$3$0.abrupt('return');

          case 22:
            context$3$0.next = 30;
            break;

          case 24:
            context$3$0.prev = 24;
            context$3$0.t0 = context$3$0['catch'](19);
            context$3$0.next = 28;
            return _regeneratorRuntime.awrap(_util.actionWith(_extends({}, requestType, {
              payload: new _errors.RequestError('[CALL_API].bailout function failed'),
              error: true
            }), [action, getState()]));

          case 28:
            context$3$0.t1 = context$3$0.sent;
            return context$3$0.abrupt('return', next(context$3$0.t1));

          case 30:
            if (!(typeof endpoint === 'function')) {
              context$3$0.next = 41;
              break;
            }

            context$3$0.prev = 31;

            endpoint = endpoint(getState());
            context$3$0.next = 41;
            break;

          case 35:
            context$3$0.prev = 35;
            context$3$0.t2 = context$3$0['catch'](31);
            context$3$0.next = 39;
            return _regeneratorRuntime.awrap(_util.actionWith(_extends({}, requestType, {
              payload: new _errors.RequestError('[CALL_API].endpoint function failed'),
              error: true
            }), [action, getState()]));

          case 39:
            context$3$0.t3 = context$3$0.sent;
            return context$3$0.abrupt('return', next(context$3$0.t3));

          case 41:
            if (!(typeof headers === 'function')) {
              context$3$0.next = 52;
              break;
            }

            context$3$0.prev = 42;

            headers = headers(getState());
            context$3$0.next = 52;
            break;

          case 46:
            context$3$0.prev = 46;
            context$3$0.t4 = context$3$0['catch'](42);
            context ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-api-middleware.util"></a>[module redux-api-middleware.util](#apidoc.module.redux-api-middleware.util)

#### <a name="apidoc.element.redux-api-middleware.util.actionWith"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.util.</span>actionWith (descriptor, args)](#apidoc.element.redux-api-middleware.util.actionWith)
- description and source-code
```javascript
function actionWith(descriptor, args) {
  return _regeneratorRuntime.async(function actionWith$(context$1$0) {
    while (1) switch (context$1$0.prev = context$1$0.next) {
      case 0:
        context$1$0.prev = 0;
        context$1$0.next = 3;
        return _regeneratorRuntime.awrap(typeof descriptor.payload === 'function' ? descriptor.payload.apply(descriptor, args) :
descriptor.payload);

      case 3:
        descriptor.payload = context$1$0.sent;
        context$1$0.next = 10;
        break;

      case 6:
        context$1$0.prev = 6;
        context$1$0.t0 = context$1$0['catch'](0);

        descriptor.payload = new _errors.InternalError(context$1$0.t0.message);
        descriptor.error = true;

      case 10:
        context$1$0.prev = 10;
        context$1$0.next = 13;
        return _regeneratorRuntime.awrap(typeof descriptor.meta === 'function' ? descriptor.meta.apply(descriptor, args) : descriptor
.meta);

      case 13:
        descriptor.meta = context$1$0.sent;
        context$1$0.next = 21;
        break;

      case 16:
        context$1$0.prev = 16;
        context$1$0.t1 = context$1$0['catch'](10);

        delete descriptor.meta;
        descriptor.payload = new _errors.InternalError(context$1$0.t1.message);
        descriptor.error = true;

      case 21:
        return context$1$0.abrupt('return', descriptor);

      case 22:
      case 'end':
        return context$1$0.stop();
    }
  }, null, this, [[0, 6], [10, 16]]);
}
```
- example usage
```shell
...
  context$3$0.next = 30;
  break;

case 24:
  context$3$0.prev = 24;
  context$3$0.t0 = context$3$0['catch'](19);
  context$3$0.next = 28;
  return _regeneratorRuntime.awrap(_util.actionWith(_extends({}, requestType, {
    payload: new _errors.RequestError('[CALL_API].bailout function failed'),
    error: true
  }), [action, getState()]));

case 28:
  context$3$0.t1 = context$3$0.sent;
  return context$3$0.abrupt('return', next(context$3$0.t1));
...
```

#### <a name="apidoc.element.redux-api-middleware.util.getJSON"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.util.</span>getJSON (res)](#apidoc.element.redux-api-middleware.util.getJSON)
- description and source-code
```javascript
function getJSON(res) {
  var contentType, emptyCodes;
  return _regeneratorRuntime.async(function getJSON$(context$1$0) {
    while (1) switch (context$1$0.prev = context$1$0.next) {
      case 0:
        contentType = res.headers.get('Content-Type');
        emptyCodes = [204, 205];

        if (!(! ~emptyCodes.indexOf(res.status) && contentType && ~contentType.indexOf('json'))) {
          context$1$0.next = 8;
          break;
        }

        context$1$0.next = 5;
        return _regeneratorRuntime.awrap(res.json());

      case 5:
        return context$1$0.abrupt('return', context$1$0.sent);

      case 8:
        context$1$0.next = 10;
        return _regeneratorRuntime.awrap(_Promise.resolve());

      case 10:
        return context$1$0.abrupt('return', context$1$0.sent);

      case 11:
      case 'end':
        return context$1$0.stop();
    }
  }, null, this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-api-middleware.util.normalizeTypeDescriptors"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.util.</span>normalizeTypeDescriptors (types)](#apidoc.element.redux-api-middleware.util.normalizeTypeDescriptors)
- description and source-code
```javascript
function normalizeTypeDescriptors(types) {
  var requestType = types[0];
  var successType = types[1];
  var failureType = types[2];

  if (typeof requestType === 'string' || typeof requestType === 'symbol') {
    requestType = { type: requestType };
  }

  if (typeof successType === 'string' || typeof successType === 'symbol') {
    successType = { type: successType };
  }
  successType = _extends({
    payload: function payload(action, state, res) {
      return getJSON(res);
    }
  }, successType);

  if (typeof failureType === 'string' || typeof failureType === 'symbol') {
    failureType = { type: failureType };
  }
  failureType = _extends({
    payload: function payload(action, state, res) {
      return getJSON(res).then(function (json) {
        return new _errors.ApiError(res.status, res.statusText, json);
      });
    }
  }, failureType);

  return [requestType, successType, failureType];
}
```
- example usage
```shell
...
endpoint = callAPI.endpoint;
headers = callAPI.headers;
method = callAPI.method;
body = callAPI.body;
credentials = callAPI.credentials;
bailout = callAPI.bailout;
types = callAPI.types;
_normalizeTypeDescriptors = _util.normalizeTypeDescriptors(types);
requestType = _normalizeTypeDescriptors[0];
successType = _normalizeTypeDescriptors[1];
failureType = _normalizeTypeDescriptors[2];
context$3$0.prev = 19;

if (!(typeof bailout === 'boolean' && bailout || typeof bailout === 'function' && bailout(getState()))) {
  context$3$0.next = 22;
...
```



# <a name="apidoc.module.redux-api-middleware.validation"></a>[module redux-api-middleware.validation](#apidoc.module.redux-api-middleware.validation)

#### <a name="apidoc.element.redux-api-middleware.validation.isRSAA"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.validation.</span>isRSAA (action)](#apidoc.element.redux-api-middleware.validation.isRSAA)
- description and source-code
```javascript
function isRSAA(action) {
  return _lodashIsplainobject2['default'](action) && action.hasOwnProperty(_CALL_API2['default']);
}
```
- example usage
```shell
...
  return function (next) {
    return function callee$2$0(action) {
      var validationErrors, _callAPI, _requestType, callAPI, endpoint, headers, method, body, credentials, bailout, types, _normalizeTypeDescriptors
, requestType, successType, failureType, res;

      return _regeneratorRuntime.async(function callee$2$0$(context$3$0) {
        while (1) switch (context$3$0.prev = context$3$0.next) {
case 0:
  if (_validation.isRSAA(action)) {
    context$3$0.next = 2;
    break;
  }

  return context$3$0.abrupt('return', next(action));

case 2:
...
```

#### <a name="apidoc.element.redux-api-middleware.validation.isValidRSAA"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.validation.</span>isValidRSAA (action)](#apidoc.element.redux-api-middleware.validation.isValidRSAA)
- description and source-code
```javascript
function isValidRSAA(action) {
  return !validateRSAA(action).length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-api-middleware.validation.isValidTypeDescriptor"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.validation.</span>isValidTypeDescriptor (obj)](#apidoc.element.redux-api-middleware.validation.isValidTypeDescriptor)
- description and source-code
```javascript
function isValidTypeDescriptor(obj) {
  var validKeys = ['type', 'payload', 'meta'];

  if (!_lodashIsplainobject2['default'](obj)) {
    return false;
  }
  for (var key in obj) {
    if (! ~validKeys.indexOf(key)) {
      return false;
    }
  }
  if (!('type' in obj)) {
    return false;
  } else if (typeof obj.type !== 'string' && typeof obj.type !== 'symbol') {
    return false;
  }

  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-api-middleware.validation.validateRSAA"></a>[function <span class="apidocSignatureSpan">redux-api-middleware.validation.</span>validateRSAA (action)](#apidoc.element.redux-api-middleware.validation.validateRSAA)
- description and source-code
```javascript
function validateRSAA(action) {
  var validationErrors = [];
  var validCallAPIKeys = ['endpoint', 'method', 'body', 'headers', 'credentials', 'bailout', 'types'];
  var validMethods = ['GET', 'HEAD', 'POST', 'PUT', 'PATCH', 'DELETE', 'OPTIONS'];
  var validCredentials = ['omit', 'same-origin', 'include'];

  if (!isRSAA(action)) {
    validationErrors.push('RSAAs must be plain JavaScript objects with a [CALL_API] property');
    return validationErrors;
  }

  for (var key in action) {
    if (key !== [_CALL_API2['default']]) {
      validationErrors.push('Invalid root key: ' + key);
    }
  }

  var callAPI = action[_CALL_API2['default']];
  if (!_lodashIsplainobject2['default'](callAPI)) {
    validationErrors.push('[CALL_API] property must be a plain JavaScript object');
  }
  for (var key in callAPI) {
    if (! ~validCallAPIKeys.indexOf(key)) {
      validationErrors.push('Invalid [CALL_API] key: ' + key);
    }
  }

  var endpoint = callAPI.endpoint;
  var method = callAPI.method;
  var headers = callAPI.headers;
  var credentials = callAPI.credentials;
  var types = callAPI.types;
  var bailout = callAPI.bailout;

  if (typeof endpoint === 'undefined') {
    validationErrors.push('[CALL_API] must have an endpoint property');
  } else if (typeof endpoint !== 'string' && typeof endpoint !== 'function') {
    validationErrors.push('[CALL_API].endpoint property must be a string or a function');
  }
  if (typeof method === 'undefined') {
    validationErrors.push('[CALL_API] must have a method property');
  } else if (typeof method !== 'string') {
    validationErrors.push('[CALL_API].method property must be a string');
  } else if (! ~validMethods.indexOf(method.toUpperCase())) {
    validationErrors.push('Invalid [CALL_API].method: ' + method.toUpperCase());
  }

  if (typeof headers !== 'undefined' && !_lodashIsplainobject2['default'](headers) && typeof headers !== 'function') {
    validationErrors.push('[CALL_API].headers property must be undefined, a plain JavaScript object, or a function');
  }
  if (typeof credentials !== 'undefined') {
    if (typeof credentials !== 'string') {
      validationErrors.push('[CALL_API].credentials property must be undefined, or a string');
    } else if (! ~validCredentials.indexOf(credentials)) {
      validationErrors.push('Invalid [CALL_API].credentials: ' + credentials);
    }
  }
  if (typeof bailout !== 'undefined' && typeof bailout !== 'boolean' && typeof bailout !== 'function') {
    validationErrors.push('[CALL_API].bailout property must be undefined, a boolean, or a function');
  }

  if (typeof types === 'undefined') {
    validationErrors.push('[CALL_API] must have a types property');
  } else if (!Array.isArray(types) || types.length !== 3) {
    validationErrors.push('[CALL_API].types property must be an array of length 3');
  } else {
    var requestType = types[0];
    var successType = types[1];
    var failureType = types[2];

    if (typeof requestType !== 'string' && typeof requestType !== 'symbol' && !isValidTypeDescriptor(requestType)) {
      validationErrors.push('Invalid request type');
    }
    if (typeof successType !== 'string' && typeof successType !== 'symbol' && !isValidTypeDescriptor(successType)) {
      validationErrors.push('Invalid success type');
    }
    if (typeof failureType !== 'string' && typeof failureType !== 'symbol' && !isValidTypeDescriptor(failureType)) {
      validationErrors.push('Invalid failure type');
    }
  }

  return validationErrors;
}
```
- example usage
```shell
...
  context$3$0.next = 2;
  break;
}

return context$3$0.abrupt('return', next(action));

          case 2:
validationErrors = _validation.validateRSAA(action);

if (!validationErrors.length) {
  context$3$0.next = 7;
  break;
}

_callAPI = action[_CALL_API2['default']];
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
