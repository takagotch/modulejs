### modulejs
---
https://github.com/lrsjng/modulejs

```js
modulejs.define('a', function(){
  return {val: 1};
});

modulejs.define('b', ['a'], function(a){
  return [a.val, a.val + 1];
});

modulejs.define('main', ['jquery', 'b'], function($, b){
  return {
    start: function(){
      console.log(b);
    }
  };
});

modulejs.define('modernizr', Modernizr);

modulejs.define('jquery', function(){
  return jQuery;
});

document.addEventListener('DOMContentLoaded', function(){
  var main = modulejs.require('main');
  main.start();
});

modulejs.define(id, fn)

modulejs.define(id, deps, fn)

modulejs.define(id, obj)

modulejs.define(id, deps, obj)

modulejs.require(id)

modulejs.require(id, mocks)

modulejs.require(id, mocks)

modulejs.require('b', {a: 'testomg'})

modulejs.state()

modulesj.log(inv)
modulejs.create()


```

```
{
  main: {
    deps: ['jquery', 'b']
    init: true
    reqd: []
    reqs: ['jquery', 'a', 'b']
  }
}
```

```
```


