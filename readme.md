### polyfill for use babel translate es6 for IE<=9 which use class super constructor

this code use babel translate to es5 and run in IE<=9,
```
class TestSuper {
    constructor() {
        console.log('TestSuper constructor');
    }
}

class Test extends TestSuper {
    constructor() {
        console.log('Test constructor');
        super();
    }
}

export default Test;
```
will course error:
```
Unable to get value of the property '***': object is null or undefined
```

use this as polyfill will fix it.

#### install
```
npm i ie-babel-class
```
then import is before any js.
see https://github.com/babel/babel/issues/3041
http://fedvic.com/2016/01/15/extendInBabel/
