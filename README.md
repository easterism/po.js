po.js
=====

Super-simple gettext translation in pure JS

Advantages
=====
1. Lightweight: ~0.5KB
2. No need in 3d-party dependencies like jQuery, Prototype etc.

Usage
=====
1. Create JSON file from PO and store it on your server in public folder. I suggest you to use this converter - https://localise.biz/free/converter/po-to-json
2. Include po.min.js to your project
```
<script src="po.min.js"></script>
```
3. Initialize your translation by calling init() method and pass link to your converted JSON file. Not pass this link for default language.
```
pojs.init('/ru.json');
```
5. In all your JS files replace all untranslated messages. po.js will find translation or will return this key otherwise.
```
pojs._('Hello world');
```
6. Simple sprintf emulation:
```
pojs._('My name is %s, and I am %s years old', ['Sasha', 24]);
```
