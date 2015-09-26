# JSD - JavaScript Dynamic
JSD is template engine for dynamic creation of JavaScript, HTML, CSS and other formats
with JavaScript.

It uses quite common syntax to mix static content and code blocks. Inside:
* _<% %>_ put your JavaScript code i.e <% for (...) { %> (don't have to specify closing })
* _<%= %>_ put your JavaScript which you want to be write into template output

See example below:
```
<%
var items = [0, 1, 2, 3, 4, 5];

for (i in items) {
%>
	<div 
		style="position: relative; transform: translate(<%= i*5 %>px, 0px);"
		onclick="window.alert('You clicked ' + <%= i %>);"
	>
	And <b><%= i %></b> should be a number
	</div>
<%
}
%>
```
# Performance
To increase performance your templates are compiled to JavaScript functions (which in turn can be
compiled to machine code), and can be reused, as simple as doing method call.

# Code is available as
* stand-alone JavaScript, for browser based, single web page applications
* node.js module for server-side templates
