phosphor-stackedpanel
=====================

[![Build Status](https://travis-ci.org/phosphorjs/phosphor-stackedpanel.svg)](https://travis-ci.org/phosphorjs/phosphor-stackedpanel?branch=master)
[![Coverage Status](https://coveralls.io/repos/phosphorjs/phosphor-stackedpanel/badge.svg?branch=master&service=github)](https://coveralls.io/github/phosphorjs/phosphor-stackedpanel?branch=master)

A Phosphor layout panel where visible children are stacked atop one another.


Package Install
---------------

**Prerequisites**
- [node](http://nodejs.org/)

```bash
npm install --save phosphor-stackedpanel
```


Source Build
------------

**Prerequisites**
- [git](http://git-scm.com/)
- [node](http://nodejs.org/)

```bash
git clone https://github.com/phosphorjs/phosphor-stackedpanel.git
cd phosphor-stackedpanel
npm install
```

**Rebuild**
```bash
npm run clean
npm run build
```


Run Tests
---------

Follow the source build instructions first.

```bash
# run tests in Firefox
npm test

# run tests in Chrome
npm run test:chrome

# run tests in IE
npm run test:ie
```


Build Docs
----------

Follow the source build instructions first.

```bash
npm run docs
```

Navigate to `docs/index.html`.


Build Example
-------------

Follow the source build instructions first.

```bash
npm run build:example
```

Navigate to `example/index.html`.


Supported Runtimes
------------------

The runtime versions which are currently *known to work* are listed below.
Earlier versions may also work, but come with no guarantees.

- IE 11+
- Firefox 32+
- Chrome 38+


Bundle for the Browser
----------------------

Follow the package install instructions first.

Any bundler that understands how to `require()` files with `.js` and `.css`
extensions can be used with this package.


Usage Examples
--------------

**Note:** This module is fully compatible with Node/Babel/ES6/ES5. Simply
omit the type declarations when using a language other than TypeScript.

This small module allows stacking widgets and changing their visibility. The
methods included in `phosphor-stackedpanel` can be combined with other widgets
to created a desktop-like experience. For instance, [Phosphor
tabs](http://phosphorjs.github.io/phosphor-tabs/api/) uses stacked panels to
implement Tabs Panel.

A simple example is shown below. The following code import the required modules
and creates some basic content fir the panel:


```typescript
import {
  StackedPanel
} from 'phosphor-stackedpanel';

import {
  Widget
} from 'phosphor-widget';

let w1 = new Widget();
let w2 = new Widget();
let w3 = new Widget();
```

The `StackedPanel()` constructor creates a new panel, where the widgets can be
added. The `.addChild()` method takes as argument a new widget which is
stacked on top of the existing ones. Toggling the visibility of each item is
straightforward with the `.hide()` and `.show()` methods. 


```
// Setup the stacked panel.
let panel = new StackedPanel();
panel.addChild(w1);
panel.addChild(w2);
panel.addChild(w3);

// Toggle the visible widgets as needed.
w1.hide();
w2.show();
w3.hide();
```


API
---

[API Docs](http://phosphorjs.github.io/phosphor-stackedpanel/api/)
