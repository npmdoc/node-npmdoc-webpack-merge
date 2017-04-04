# api documentation for  [webpack-merge (v4.1.0)](https://github.com/survivejs/webpack-merge)  [![npm package](https://img.shields.io/npm/v/npmdoc-webpack-merge.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-webpack-merge) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-webpack-merge.svg)](https://travis-ci.org/npmdoc/node-npmdoc-webpack-merge)
#### Variant of merge that's useful for webpack configuration

[![NPM](https://nodei.co/npm/webpack-merge.png?downloads=true)](https://www.npmjs.com/package/webpack-merge)

[![apidoc](https://npmdoc.github.io/node-npmdoc-webpack-merge/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-webpack-merge_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-webpack-merge/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-webpack-merge/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-webpack-merge/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Juho Vepsalainen",
        "email": "bebraw@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/survivejs/webpack-merge/issues"
    },
    "dependencies": {
        "lodash": "^4.17.4"
    },
    "description": "Variant of merge that's useful for webpack configuration",
    "devDependencies": {
        "babel-cli": "^6.18.0",
        "babel-plugin-lodash": "^3.2.11",
        "babel-preset-es2015": "^6.18.0",
        "copy-webpack-plugin": "^4.0.1",
        "eslint": "^3.13.1",
        "eslint-config-airbnb": "^14.0.0",
        "eslint-plugin-import": "^2.2.0",
        "eslint-plugin-jsx-a11y": "^3.0.2",
        "eslint-plugin-react": "^6.9.0",
        "git-prepush-hook": "^1.0.1",
        "istanbul": "^0.4.5",
        "mocha": "^3.2.0",
        "npm-watch": "^0.1.7",
        "webpack": "^1.14.0"
    },
    "directories": {},
    "dist": {
        "shasum": "6ad72223b3e0b837e531e4597c199f909361511e",
        "tarball": "https://registry.npmjs.org/webpack-merge/-/webpack-merge-4.1.0.tgz"
    },
    "files": [
        "lib"
    ],
    "gitHead": "d9559b9d28deecd1d7887aeef67a41180b66eb78",
    "homepage": "https://github.com/survivejs/webpack-merge",
    "keywords": [
        "webpack",
        "merge"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "bebraw",
            "email": "bebraw@gmail.com"
        }
    ],
    "name": "webpack-merge",
    "optionalDependencies": {},
    "pre-push": [
        "test:lint",
        "build",
        "test"
    ],
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/survivejs/webpack-merge.git"
    },
    "scripts": {
        "build": "babel src -d lib",
        "preversion": "npm run test:lint && npm run build && npm test && git commit --allow-empty -am \"Update lib\"",
        "test": "mocha tests/test-*",
        "test:coverage": "istanbul cover node_modules/.bin/_mocha tests/test-*",
        "test:lint": "eslint src/ tests/ --cache",
        "watch": "npm-watch"
    },
    "version": "4.1.0",
    "watch": {
        "build": {
            "patterns": [
                "src/**/*.js"
            ]
        },
        "test": {
            "patterns": [
                "src/**/*.js",
                "tests/**/*.js"
            ]
        },
        "test:lint": {
            "patterns": [
                "src/**/*.js",
                "tests/**/*.js"
            ]
        }
    }
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module webpack-merge](#apidoc.module.webpack-merge)
1.  [function <span class="apidocSignatureSpan">webpack-merge.</span>multiple ()](#apidoc.element.webpack-merge.multiple)
1.  [function <span class="apidocSignatureSpan">webpack-merge.</span>smart ()](#apidoc.element.webpack-merge.smart)
1.  [function <span class="apidocSignatureSpan">webpack-merge.</span>smartStrategy ()](#apidoc.element.webpack-merge.smartStrategy)
1.  [function <span class="apidocSignatureSpan">webpack-merge.</span>strategy ()](#apidoc.element.webpack-merge.strategy)
1.  [function <span class="apidocSignatureSpan">webpack-merge.</span>unique (key, uniques)](#apidoc.element.webpack-merge.unique)
1.  object <span class="apidocSignatureSpan">webpack-merge.</span>join_arrays
1.  object <span class="apidocSignatureSpan">webpack-merge.</span>join_arrays_smart

#### [module webpack-merge.join_arrays](#apidoc.module.webpack-merge.join_arrays)
1.  [function <span class="apidocSignatureSpan">webpack-merge.join_arrays.</span>default ()](#apidoc.element.webpack-merge.join_arrays.default)

#### [module webpack-merge.join_arrays_smart](#apidoc.module.webpack-merge.join_arrays_smart)
1.  [function <span class="apidocSignatureSpan">webpack-merge.join_arrays_smart.</span>uniteEntries (newEntry, entry)](#apidoc.element.webpack-merge.join_arrays_smart.uniteEntries)
1.  [function <span class="apidocSignatureSpan">webpack-merge.join_arrays_smart.</span>uniteRules (rules, key, newRule, rule)](#apidoc.element.webpack-merge.join_arrays_smart.uniteRules)

#### [module webpack-merge.unique](#apidoc.module.webpack-merge.unique)
1.  [function <span class="apidocSignatureSpan">webpack-merge.unique.</span>default (key, uniques)](#apidoc.element.webpack-merge.unique.default)



# <a name="apidoc.module.webpack-merge"></a>[module webpack-merge](#apidoc.module.webpack-merge)

#### <a name="apidoc.element.webpack-merge.multiple"></a>[function <span class="apidocSignatureSpan">webpack-merge.</span>multiple ()](#apidoc.element.webpack-merge.multiple)
- description and source-code
```javascript
function mergeMultiple() {
  for (var _len3 = arguments.length, sources = Array(_len3), _key3 = 0; _key3 < _len3; _key3++) {
    sources[_key3] = arguments[_key3];
  }

  return (0, _values3.default)(merge(sources));
}
```
- example usage
```shell
...
loader: 'coffee'
  }]
}
'''

## Multiple Merging

### **'merge.multiple(...configuration | [...configuration])'**

Sometimes you may need to support multiple targets, *webpack-merge* will accept an object where each key represents the target configuration
. The output becomes an *array* of configurations where matching keys are merged and non-matching keys are added.

'''javascript
var path = require('path');
var baseConfig = {
server: {
...
```

#### <a name="apidoc.element.webpack-merge.smart"></a>[function <span class="apidocSignatureSpan">webpack-merge.</span>smart ()](#apidoc.element.webpack-merge.smart)
- description and source-code
```javascript
smart = function () {
  for (var _len2 = arguments.length, structures = Array(_len2), _key2 = 0; _key2 < _len2; _key2++) {
    structures[_key2] = arguments[_key2];
  }

  if (Array.isArray(structures[0])) {
    return _mergeWith3.default.apply(undefined, [{}].concat(_toConsumableArray(structures[0]), [(0, _joinArrays2.default)(sources
[0])]));
  }

  return _mergeWith3.default.apply(undefined, [{}].concat(structures, [(0, _joinArrays2.default)(sources[0])]));
}
```
- example usage
```shell
...
    'module.loaders': 'prepend'
  }
)(object1, object2, object3, ...);
'''

## Smart Merging

### **'merge.smart(...configuration | [...configuration])'**

*webpack-merge* tries to be smart about merging loaders when 'merge.smart' is used. Loaders with matching tests will be merged into
 a single loader value.

Note that the logic picks up webpack 2 'rules' kind of syntax as well. The examples below have been written in webpack 1 syntax.

**package.json**
...
```

#### <a name="apidoc.element.webpack-merge.smartStrategy"></a>[function <span class="apidocSignatureSpan">webpack-merge.</span>smartStrategy ()](#apidoc.element.webpack-merge.smartStrategy)
- description and source-code
```javascript
function mergeSmartStrategy() {
  var rules = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : {};
  return merge({
    customizeArray: function customizeArray(a, b, key) {
      var topKey = key.split('.').slice(-1)[0];

      if (isRule(topKey)) {
        switch (rules[key]) {
          case 'prepend':
            return [].concat(_toConsumableArray((0, _differenceWith3.default)(b, a, function (newRule, seenRule) {
              return (0, _joinArraysSmart.uniteRules)(rules, key, newRule, seenRule, 'prepend');
            })), _toConsumableArray(a));
          case 'replace':
            return b;
          default:
            // append
            return (0, _unionWith3.default)(a, b, _joinArraysSmart.uniteRules.bind(null, rules, key));
        }
      }

      return _customizeArray(rules)(a, b, key);
    },
    customizeObject: customizeObject(rules)
  });
}
```
- example usage
```shell
...
{
  entry: 'prepend', // or 'replace', defaults to 'append'
  'module.loaders': 'prepend'
}
)(object1, object2, object3, ...);
'''

### **'merge.smartStrategy({ <key>: '<prepend|append|replace>''})(...configuration | [...configuration])'**

The same idea works with smart merging too (described below in greater detail).

'''javascript
var output = merge.smartStrategy(
{
  entry: 'prepend', // or 'replace'
...
```

#### <a name="apidoc.element.webpack-merge.strategy"></a>[function <span class="apidocSignatureSpan">webpack-merge.</span>strategy ()](#apidoc.element.webpack-merge.strategy)
- description and source-code
```javascript
function mergeStrategy() {
  var rules = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : {};
  return merge({
    customizeArray: _customizeArray(rules),
    customizeObject: customizeObject(rules)
  });
}
```
- example usage
```shell
...
});

// Output contains only single HotModuleReplacementPlugin now.
'''

## Merging with Strategies

### **'merge.strategy({ <field>: '<prepend|append|replace>''})(...configuration | [...configuration])'**

Given you may want to configure merging behavior per field, there's a strategy variant:

'''javascript
// Merging with a specific merge strategy
var output = merge.strategy(
{
...
```

#### <a name="apidoc.element.webpack-merge.unique"></a>[function <span class="apidocSignatureSpan">webpack-merge.</span>unique (key, uniques)](#apidoc.element.webpack-merge.unique)
- description and source-code
```javascript
function mergeUnique(key, uniques) {
  var getter = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : function (a) {
    return a;
  };

  return function (a, b, k) {
    return k === key && [].concat(_toConsumableArray(a), _toConsumableArray((0, _differenceWith3.default)(b, a, function (item) {
      return uniques.indexOf(getter(item)) >= 0;
    })));
  };
}
```
- example usage
```shell
...
    // Fall back to default merging
    return undefined;
  }
}
)(object1, object2, object3, ...);
'''

### **'merge.unique(<field>, <fields>, field => field)'**

'''javascript
const output = merge({
customizeArray: merge.unique(
  'plugins',
  ['HotModuleReplacementPlugin'],
  plugin => plugin.constructor && plugin.constructor.name
...
```



# <a name="apidoc.module.webpack-merge.join_arrays"></a>[module webpack-merge.join_arrays](#apidoc.module.webpack-merge.join_arrays)

#### <a name="apidoc.element.webpack-merge.join_arrays.default"></a>[function <span class="apidocSignatureSpan">webpack-merge.join_arrays.</span>default ()](#apidoc.element.webpack-merge.join_arrays.default)
- description and source-code
```javascript
function joinArrays() {
  var _ref = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : {},
      customizeArray = _ref.customizeArray,
      customizeObject = _ref.customizeObject,
      key = _ref.key;

  return function _joinArrays(a, b, k) {
    var newKey = key ? key + '.' + k : k;

    if ((0, _isFunction3.default)(a) && (0, _isFunction3.default)(b)) {
      return function () {
        return _joinArrays(a.apply(undefined, arguments), b.apply(undefined, arguments), k);
      };
    }
    if (isArray(a) && isArray(b)) {
      var customResult = customizeArray && customizeArray(a, b, newKey);

      return customResult || [].concat(_toConsumableArray(a), _toConsumableArray(b));
    }

    if ((0, _isPlainObject3.default)(a) && (0, _isPlainObject3.default)(b)) {
      var _customResult = customizeObject && customizeObject(a, b, newKey);

      return _customResult || (0, _mergeWith3.default)({}, a, b, joinArrays({
        customizeArray: customizeArray,
        customizeObject: customizeObject,
        key: newKey
      }));
    }

    if ((0, _isPlainObject3.default)(b)) {
      return (0, _cloneDeep3.default)(b);
    }

    return b;
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack-merge.join_arrays_smart"></a>[module webpack-merge.join_arrays_smart](#apidoc.module.webpack-merge.join_arrays_smart)

#### <a name="apidoc.element.webpack-merge.join_arrays_smart.uniteEntries"></a>[function <span class="apidocSignatureSpan">webpack-merge.join_arrays_smart.</span>uniteEntries (newEntry, entry)](#apidoc.element.webpack-merge.join_arrays_smart.uniteEntries)
- description and source-code
```javascript
function uniteEntries(newEntry, entry) {
  var loaderNameRe = /^([^?]+)/ig;

  var _entry$loader$match = entry.loader.match(loaderNameRe),
      _entry$loader$match2 = _slicedToArray(_entry$loader$match, 1),
      loaderName = _entry$loader$match2[0];

  var _newEntry$loader$matc = newEntry.loader.match(loaderNameRe),
      _newEntry$loader$matc2 = _slicedToArray(_newEntry$loader$matc, 1),
      newLoaderName = _newEntry$loader$matc2[0];

  if (loaderName !== newLoaderName) {
    return false;
  }

  // Replace query values with newer ones
  (0, _mergeWith3.default)(entry, newEntry);
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack-merge.join_arrays_smart.uniteRules"></a>[function <span class="apidocSignatureSpan">webpack-merge.join_arrays_smart.</span>uniteRules (rules, key, newRule, rule)](#apidoc.element.webpack-merge.join_arrays_smart.uniteRules)
- description and source-code
```javascript
function uniteRules(rules, key, newRule, rule) {
  if (String(rule.test) !== String(newRule.test) || (newRule.enforce || rule.enforce) && rule.enforce !== newRule.enforce || newRule
.include && !isSameValue(rule.include, newRule.include) || newRule.exclude && !isSameValue(rule.exclude, newRule.exclude)) {
    return false;
  } else if (!rule.test && !rule.include && !rule.exclude && (rule.loader && rule.loader.split('?')[0]) !== (newRule.loader && newRule
.loader.split('?')[0])) {
    // Don't merge the rule if there isn't any identifying fields and the loaders don't match
    return false;
  } else if ((rule.include || rule.exclude) && !newRule.include && !newRule.exclude) {
    // Don't merge child without include/exclude to parent that has either
    return false;
  }

  // newRule.loader should always override
  if (newRule.loader) {
    var optionsKey = newRule.options ? 'options' : newRule.query && 'query';

    delete rule.use;
    delete rule.loaders;
    rule.loader = newRule.loader;

    if (optionsKey) {
      rule[optionsKey] = newRule[optionsKey];
    }
  } else if ((rule.use || rule.loaders || rule.loader) && (newRule.use || newRule.loaders)) {
    var expandEntry = function expandEntry(loader) {
      return typeof loader === 'string' ? { loader: loader } : loader;
    };
    // this is only here to avoid breaking existing tests
    var unwrapEntry = function unwrapEntry(entry) {
      return !entry.options && !entry.query ? entry.loader : entry;
    };

    var entries = void 0;
    if (rule.loader) {
      var _optionsKey = rule.options ? 'options' : rule.query && 'query';
      entries = [{ loader: rule.loader }];

      if (_optionsKey) {
        entries[0][_optionsKey] = rule[_optionsKey];
      }

      delete rule.loader;

      if (_optionsKey) {
        delete rule[_optionsKey];
      }
    } else {
      entries = [].concat(rule.use || rule.loaders).map(expandEntry);
    }
    var newEntries = [].concat(newRule.use || newRule.loaders).map(expandEntry);

    var loadersKey = rule.use || newRule.use ? 'use' : 'loaders';
    var resolvedKey = key + '.' + loadersKey;

    switch (rules[resolvedKey]) {
      case 'prepend':
        rule[loadersKey] = [].concat(_toConsumableArray((0, _differenceWith3.default)(newEntries, entries, uniteEntries)), _toConsumableArray
(entries)).map(unwrapEntry);
        break;
      case 'replace':
        rule[loadersKey] = newRule.use || newRule.loaders;
        break;
      default:
        rule[loadersKey] = (0, _unionWith3.default)(
        // Remove existing entries so that we can respect the order of the new
        // entries
        (0, _differenceWith3.default)(entries, newEntries, _isEqual3.default), newEntries, uniteEntries).map(unwrapEntry);
    }
  }

  if (newRule.include) {
    rule.include = newRule.include;
  }

  if (newRule.exclude) {
    rule.exclude = newRule.exclude;
  }

  return true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack-merge.unique"></a>[module webpack-merge.unique](#apidoc.module.webpack-merge.unique)

#### <a name="apidoc.element.webpack-merge.unique.default"></a>[function <span class="apidocSignatureSpan">webpack-merge.unique.</span>default (key, uniques)](#apidoc.element.webpack-merge.unique.default)
- description and source-code
```javascript
function mergeUnique(key, uniques) {
  var getter = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : function (a) {
    return a;
  };

  return function (a, b, k) {
    return k === key && [].concat(_toConsumableArray(a), _toConsumableArray((0, _differenceWith3.default)(b, a, function (item) {
      return uniques.indexOf(getter(item)) >= 0;
    })));
  };
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
