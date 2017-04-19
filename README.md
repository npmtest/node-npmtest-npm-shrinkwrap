# npmtest-npm-shrinkwrap

#### basic test coverage for  [npm-shrinkwrap (v6.0.2)](https://github.com/uber/npm-shrinkwrap)  [![npm package](https://img.shields.io/npm/v/npmtest-npm-shrinkwrap.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-npm-shrinkwrap) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-npm-shrinkwrap.svg)](https://travis-ci.org/npmtest/node-npmtest-npm-shrinkwrap)

#### A consistent shrinkwrap tool

[![NPM](https://nodei.co/npm/npm-shrinkwrap.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/npm-shrinkwrap)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-npm-shrinkwrap/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-npm-shrinkwrap/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/test-report.html](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-npm-shrinkwrap/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-npm-shrinkwrap/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-npm-shrinkwrap/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-npm-shrinkwrap/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-npm-shrinkwrap/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "npm-shrinkwrap",
    "version": "6.0.2",
    "description": "A consistent shrinkwrap tool",
    "keywords": [],
    "author": {
        "name": "Raynos"
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/uber/npm-shrinkwrap.git"
    },
    "main": "index",
    "homepage": "https://github.com/uber/npm-shrinkwrap",
    "bugs": {
        "url": "https://github.com/uber/npm-shrinkwrap/issues"
    },
    "dependencies": {
        "array-find": "^0.1.1",
        "array-flatten": "^2.1.0",
        "error": "^4.2.0",
        "graceful-fs": "^4.1.2",
        "json-diff": "^0.3.1",
        "minimist": "^1.1.0",
        "msee": "^0.1.1",
        "npm": "^2.15.10",
        "rimraf": "^2.2.8",
        "run-parallel": "^1.1.6",
        "run-series": "^1.0.2",
        "safe-json-parse": "^2.0.0",
        "semver": "^4.0.3",
        "sorted-object": "^1.0.0",
        "string-template": "^0.2.0"
    },
    "devDependencies": {
        "fixtures-fs": "^2.0.0",
        "istanbul": "~0.3.2",
        "jshint": "2.5.6",
        "pre-commit": "0.0.9",
        "tap-spec": "~1.0.0",
        "tape": "^3.0.2"
    },
    "scripts": {
        "test": "npm run jshint -s && NODE_ENV=test node test/index.js | tap-spec",
        "unit-test": "NODE_ENV=test node test/npm-shrinkwrap.js | tap-spec",
        "jshint-pre-commit": "jshint --verbose $(git diff --cached --name-only | grep '\\.js$')",
        "jshint": "jshint --verbose .",
        "cover": "istanbul cover --report none --print detail test/index.js",
        "view-cover": "istanbul report html && open ./coverage/index.html",
        "travis": "npm run cover -s && istanbul report lcov && ((cat coverage/lcov.info | coveralls) || exit 0)"
    },
    "pre-commit": [
        "jshint-pre-commit",
        "unit-test"
    ],
    "bin": {
        "npm-shrinkwrap": "./bin/cli.js"
    },
    "license": "MIT",
    "engine": {
        "node": ">= 0.10.x"
    },
    "gitHead": "b2be60f225966dc7353ea4ce2edc9fb04a184740",
    "dist": {
        "shasum": "0a4e269bcc64fdb1741a2c46c2b0457a0072d437",
        "tarball": "https://registry.npmjs.org/npm-shrinkwrap/-/npm-shrinkwrap-6.0.2.tgz"
    },
    "maintainers": [
        {
            "name": "raynos"
        },
        {
            "name": "uber"
        }
    ],
    "directories": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
