bdsm
==========

Bad ass server mocks

[![Build Status](https://travis-ci.org/500tech/bdsm.svg?branch=master)](https://travis-ci.org/500tech/bdsm)
[![npm version](https://badge.fury.io/js/bdsmjs.svg)](https://badge.fury.io/js/bdsmjs)

![short introduction](http://500tech.github.io/bdsm/assets/images/bdsm_intro.gif)

Using BDSM in your project
--------------------------

Add to your packages:

    npm install bdsm --save

Require in your app:

    import 'bdsm';

Once you reload the application, the BDSM logo will appear in bottom
right corner.

Enjoy!


Using Mocks tracked by git
==========================
If you want to use mocks which will be committed into git and you're using webpack you can use the following code to import the mocks on application start:

```
import bdsm from 'bdsmjs';
const mocks = require.context(__dirname + '/mocks', true, /\.json$/);
mocks.keys().forEach((key) => bdsm.import(JSON.stringify(mocks(key))));
```

This assumes your mocks are placed in the mocks directory which is located at the root of the project.
In the mocks directory you have exports for either complete scenarios or separate mock requests.


Contributing to BDSM
--------------------


1. Clone the repo
1. Install dependencies (at the root of the repo):

    ```
    npm install
    ```

1. Run the project

    ```
    npm start
    ```

1. Build for deployment

    ```
    npm run build
    ```
