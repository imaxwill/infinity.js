infinity.js
---
***Information:***
<br>
infinity.js is a javascript library with practicality in mind. It's tight-nit, to the point, and it has more features than even jQuery.
<br><br>
***Usage:***
<br>
Add this script inside your document:
```
<script src="/path/to/infinity.js" var=""></script>
```
And set the `var` attribute to a string representing the object you want the library's methods to be applied to.
<br><br>
***Example:***
<br>
*Hello World: (Google Chrome)*
```
<script src="/path/to/infinity.js" var="i420">
	i420.prompt({
		label: "Hello World", run: function (a) {
			if (a.response == "") {
				i420.run(console.log, "They Didn't Respond.");
			}
		}
	});
</script>
```
***Example:***
<br>
*Clipboard To Console: (Electron)*
```
<script src="/path/to/infinity.js" var="@library" /* accelerator="true" */>
	window["@library"].exec({
		context: require("electron").clipboard, details: [window["@library"], run: function (a) {
			var a.root.original = this.readText(); var loop = a.loop({
				interval: 50, delay: 50, context: this, run: function () {
					var current = this.readText(); if (current != original) {
						console.log(current); a.root.original = current;
					}
				}
			});
		}
	});
</script>
```
