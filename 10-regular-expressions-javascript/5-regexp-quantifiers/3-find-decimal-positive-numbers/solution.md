

Целое число -- это `pattern:\d+`.

Десятичная точка с дробной частью -- `pattern:\.\d+`.

Она не обязательна, так что обернём её в скобки с квантификатором `pattern:'?'`.

Итого, получилось регулярное выражение `pattern:\d+(\.\d+)?`:

```js run
var re = /\d+(\.\d+)?/g

var str = "1.5 0 12. 123.4.";

alert( str.match(re) );   // 1.5, 0, 12, 123.4
```

