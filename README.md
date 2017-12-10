# jsdiagram-ext

This chrome extension uses the [JS Sequence Diagrams](https://bramp.github.io/js-sequence-diagrams/)
library to automatically render sequence diagrams found on any page.

To show a diagram, the page should include code like:
```
<pre lang="javascript-diagram"><code>
A --> B: pass a message
B --> A: return a message
</code></pre>
```

Note that the `lang=javascript-diagram` signals that the code contents should be rendered.
When editing markdown, you would use the triple quote syntax, like:

<pre>```javascript-diagram
Title: you diagram is here
```
</pre>

Here is an example diagram source:
```
# How to fetch a web page
Title: Typical dynamic web page request lifecycle
Browser -> Server: Browser issues GET request
Server -> Database: Server requests data
Database --> Server: Returns persistent data
Note right of Server: Server generates\ndynamic page
Server --> Browser: Returns page content
```
When this extension is active, the diagram will render below:

```javascript-diagram
# How to fetch a web page
Title: Typical dynamic web page request lifecycle
Browser -> Server: Browser issues GET request
Server -> Database: Server requests data
Database --> Server: Returns persistent data
Note right of Server: Server generates\ndynamic page
Server --> Browser: Returns page content
```
