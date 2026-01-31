## JstupidHash 256-Bit Message Digest
### A table-driven Message Digest (Hash routine) for either vanilla Javascript or Js-like languages. There are no 'blocks' needed for processing, so it really acts like a stream digest with a minimal 15-round mix as an endgame.

### THIS IS NOT A SECURE HASH! THIS IS INTENDED TO BE USED ONLY AS A LIGHTWEIGHT Js HASHING ROUTINE; IT IS NOT TO BE USED ALONGSIDE MODERN CRYPTOGRAPHICALLY SECURE ALGORITHMS!

### This is just how simple it is to use...
---
#### Reference the class (or just use it inline)
````javascript
<script src="jsh256class.js"></script>
````
---
#### Usage(Hex String Output):
```javascript
const myjsh = new JsH256();
let   mystr = "Hello World!";
/*can take either a String or Uint8Array as
  the first argument to .getDigest
*/
console.log(myjsh.getDigest(mystr));
```
#### Output:
```javascript
"cff07033de22900642723a130a3fbcc9b81b5fa4741d0e37308ef69edca80dec"
```
---
#### Usage(Bytes Output):
```javascript
const myjsh = new JsH256();
let   mystr = "Hello World!";
console.log(myjsh.getDigest(mystr, true));
```
#### Output:
```javascript
Uint8Array(32) [ 207, 240, 112, 51, 222, 34, 144, 6, 66, 114, … ]
```
