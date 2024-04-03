#                                                       JAVASCRIPT STRING METHODS
JavaScript string methods are built-in functions that operate on strings, allowing developers to manipulate, transform, or extract information from strings easily. These methods are part of the String object and can be accessed through any string variable or literal by using dot notation.

**Basic string Methods**
sring sameer
String length
String charAt()
String charCodeAt()
String at()
String [ ]
String slice()
String substring()
String substr()
String toUpperCase()
String toLowerCase()
String concat()
String trim()
String trimStart()
String trimEnd()
String padStart()
String padEnd()
String repeat()
String replace()
String replaceAll()
String split()

**1.JAVASCRIPT STRING LENGHT**


JavaScript's length property for strings returns the number of characters in a string. Here's a simple explanation with a code example

```bash
let myString = "Hello, World!";

let lengthOfString = myString.length;

console.log("Length of the string:", lengthOfString);
```

**2.Extracting String Characters**

There are 4 methods for extracting string characters:

The at(position) Method
The charAt(position) Method
The charCodeAt(position) Method
Using property access [] like in arrays

**2.1  JavaScript String charAt()**

The charAt() method in JavaScript returns the character at a specified index within a string.

let myString = "Hello";

let charAtIndex1 = myString.charAt(1);

console.log("Character at index 1:", charAtIndex1);

```bash
let myString = "Hello";

let charAtIndex1 = myString.charAt(1);

console.log("Character at index 1:", charAtIndex1);
```
**2.2 JavaScript String charCodeAt()**

The charCodeAt() method in JavaScript returns the Unicode value of the character at a specified index within a string.

```bash

let myString = "Hello";

let charCodeAt1 = myString.charCodeAt(1);

console.log("Unicode value of character at index 1:", charCodeAt1);
```

**2.3 JavaScript String at()**

The at() method returns the character at a specified index (position) in a string.

The at() method is supported in all modern browsers since March 2022:

```bash
const name = "W3Schools";
let letter = name.at(2);

console.log(letter);
```

**2.4 Property Acess STRING[]**
```bash
const name = "W3Schools";
let letter = name[2];
console.log(letter);
```
**3.Extracting String Parts**
There are 3 methods for extracting a part of a string:

slice(start, end)
substring(start, end)
substr(start, length)

**3.1 JavaScript String slice()**
slice() extracts a part of a string and returns the extracted part in a new string.
```bash
let text = "Apple, Banana, Kiwi";
let part = text.slice(7,13);
console.log(part);
```

**3.2 JavaScript String substring()**

substring() is similar to slice().

The difference is that start and end values less than 0 are treated as 0 in substring().
```bash
let str = "Apple, Banana, Kiwi";
let part = str.substring(-7,13);
console.log(part);
```
**3.3 JavaScript String substr()**

substr() is similar to slice().

The difference is that the second parameter specifies the length of the extracted part.

```bash
let str = "Apple, Banana, Kiwi";
let part = str.substr(7,6);
console.log(part);
```
**4.converting uppercase and lower case**
A string is converted to upper case with toUpperCase():

A string is converted to lower case with toLowerCase():

**4.1 JavaScript String toUpperCase()**
<!DOCTYPE html>
<html>
<body>

<h1>JavaScript String Methods</h1>
<p>Convert string to upper case:</p>

<button onclick="myFunction()">Try it</button>

<p id="demo">Hello World!</p>

```bash
<script>
function myFunction() {
  let text = document.getElementById("demo").innerHTML;
  document.getElementById("demo").innerHTML =
  text.toUpperCase();
}
</script>

</body>
</html>
```
**4.2 javascript string tolowercase()**
```bash
<!DOCTYPE html>
<html>
<body>

<h1>JavaScript String Methods</h1>
<p>Convert string to lower case:</p>

<button onclick="myFunction()">Try it</button>

<p id="demo">Hello World!</p>

<script>
function myFunction() {
  let text = document.getElementById("demo").innerHTML;
  document.getElementById("demo").innerHTML =
  text.toLowerCase();
}
</script>

</body>
</html>
```
**5. JavaScript String concat()**
concat() joins two or more strings

```bash
let text1 = "Hello";
let text2 = "World!";
let text3 = text1.concat(" ",text2);
console.log(text3);
```

**6.javascript string trim**
The trim() method removes whitespace from both sides of a string:'
```bash
let text1 = "     Hello World!     ";
let text2 = text1.trim();

console.log(text1)
console.log(text2)
```

**6.1 javascript string trimstart()**

The trimStart() method works like trim(), but removes whitespace only from the start of a string.



```bash
<!DOCTYPE html>
<html>
<body>

<h1>JavaScript Strings</h1>
<h2>The trimStart() Method</h2>

<p id="demo"></p>

<script>
let text1 = "     Hello World!     ";
let text2 = text1.trimStart();

document.getElementById("demo").innerHTML =
"Length text1 = " + text1.length + "<br>Length text2 = " + text2.length;
</script>
```

</body>
</html>

**6.2JavaScript String trimEnd()**

The trimEnd() method works like trim(), but removes whitespace only from the end of a string
```bash
let text1 = "     hello     ";
let text2 = text1.trimend();
console.log(text1);
console.log(text2);
```


**7.JavaScript String Padding**

The padStart() method pads a string from the start.

```bash
let text = "5";
text1 = text.padStart(2,"44");
console.log(text1)
```
**7.1 JavaScript String padEnd()**
The padEnd() method pads a string from the end

```bash
let text = "5";
text1 = text.padEnd(2,"44");
console.log(text1)
```

**8.JavaScript String repeat()**

The repeat() method returns a string with a number of copies of a string.

The repeat() method returns a new string.

```bash
let text = "Hello world!";
let result = text.repeat(2);
console.log(result);
```
**9.Replacing String Content**

The replace() method replaces a specified value with another value in a string:

To replace case insensitive, use a regular expression with an /i flag (insensitive):

To replace all matches, use a regular expression with a /g flag (global match):

```bash
<!DOCTYPE html>
<html>

<body>

<h1>JavaScript String Methods</h1>
<p>Replace "Microsoft" with "W3Schools" in the paragraph below:</p>

<button onclick="myFunction()">Try it</button>

<p id="demo">Please visit Microsoft!</p>

<script>
function myFunction() {
  let text = document.getElementById("demo").innerHTML;
  document.getElementById("demo").innerHTML =
  text.replace("Microsoft","W3Schools");
}
</script>

</body>
</html>
```

**9.1 Replace ALL()**

The replaceAll() method allows you to specify a regular expression instead of a string to be replaced

```bash
<!DOCTYPE html>
<html>
<body>
<h1>JavaScript Strings</h1>
<h2>The replaceAll() Method</h2>

<p>ES2021 intoduced the string method replaceAll().</p>

<p id="demo"></p>

<script>
let text = "I love cats. Cats are very easy to love. Cats are very popular."
text = text.replaceAll("Cats","Dogs");
text = text.replaceAll("cats","dogs");

document.getElementById("demo").innerHTML = text;
</script>

</body>
</html>
```

**10.JavaScript String split()**

A string can be converted to an array with the split() method:
```bash
const word = "hello";
const characters = word.split("");
console.log(characters);
```








