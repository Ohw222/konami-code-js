# KonamiCodeJS #

Fire a JavaScript Event when you enter the « Up Up Bottom Bottom Left Right Left Right B A » Konami Code Sequence.





## API Documentation ##
<a name="KonamiCode"></a>

**Version**: 0.4.0
**Author:** [Bruno Lesieur](http://www.lesieur.name/)

* [KonamiCode](#KonamiCode)
    * [new KonamiCode([options])](#new_KonamiCode_new)
    * _instance_
        * [.enable()](#KonamiCode+enable)
        * [.disable()](#KonamiCode+disable)
        * [.setListener(listener)](#KonamiCode+setListener)
        * [.setCallback(callback)](#KonamiCode+setCallback)
    * _static_
        * [.noConflict()](#KonamiCode.noConflict)

<a name="new_KonamiCode_new"></a>

### new KonamiCode([options])
Create Konami Code Sequence recognition « Up Up Bottom Bottom Left Right Left Right B A » on specific HTMLElement or on global HTMLDocument.


| Param | Type | Description |
| --- | --- | --- |
| [options] | <code>Object</code> &#124; <code>function</code> | Container for all options. If type of `options` is Function, it is executed after Konami Code Sequence has been recognize. |
| [options.callback] | <code>function</code> | If `options` is not a Function, `options.callback` is executed after Konami Code Sequence has been entered. |
| [options.listener] | <code>Node</code> | By default it is the HTMLDocument `window.document`. You can pass some HTMLElement like `<input>` (HTMLInputElement) to only recognize Konami Code Sequence from this element. |
| [options.debug] | <code>boolean</code> | By default it is set to `false`. When you set this value to `true`, that allows you to see all debug message in the console. |

<a name="KonamiCode+enable"></a>

### konamiCode.enable()
Active the listening of Konami Code Sequence.

<a name="KonamiCode+disable"></a>

### konamiCode.disable()
Unactive the listening of Konami Code Sequence.

<a name="KonamiCode+setListener"></a>

### konamiCode.setListener(listener)
Change the listener. The old listener will no longer work. Note: change the listener enable this instance if it is previously `disable()`.


| Param | Type | Description |
| --- | --- | --- |
| listener | <code>Node</code> | You can pass some HTMLElement like `<input>` (HTMLInputElement) to only recognize Konami Code Sequence from this element. |

<a name="KonamiCode+setCallback"></a>

### konamiCode.setCallback(callback)
Change the Function executed after Konami Code Sequence has been entered.


| Param | Type | Description |
| --- | --- | --- |
| callback | <code>function</code> | Function executed after Konami Code Sequence has been entered. |

<a name="KonamiCode.noConflict"></a>

### KonamiCode.noConflict()
If a previous `KonamiCode` variable exist into global environment, you could kept it by changing name of current KonamiCode.
You can also just use that function to change the name of Global « KonamiCode » variable.

**Example**
```js
<script src="other/konami-code.js"></script>
<script src="last/konami-code.js"></script>
<script>
 	var MyKC = KonamiCode.noConflict();
 	console.log(KonamiCode); // Return the other KonamiCode
 	console.log(MyKC); // Return your KonamiCode
</script>
```





## Import JavaScript File ##

### From CDN ###

- For development:

```html
<script src="https://rawgit.com/Haeresis/konami-code-js/master/src/konami-code.js"></script>
```

- For production:

```html
<script src="https://cdn.rawgit.com/Haeresis/konami-code-js/master/src/konami-code.js"></script>
```

### With AMD Loader ###

```html
<script src="require.js"></script>
<script>
	requirejs(["konami-code"], function (KonamiCode) {
	    new KonamiCode(function () {
	    	console.log("My Ester Egg !");
	    });
	});
</script>
```