# my-javascript-snippets
A snippet system list to JavaScript in Visual Studio Code

1."Arrow function with params" --> "afunp"
2."Arrow function without params" --> "afun"
3."Show an item list" --> "rvc"
4."Create html element from JavaScript" --> "create"
5."Array list with an object" --> "arr"
6."Array list object" --> "arro"
7."Call function" --> "callf"
8."Get view in const or let" --> "getv"
9."Call and get view in let" --> "getvl"
10."Call and get view in const" --> "getvc"
11."Call view and set eventListener" --> "getve"
12."Set eventListener on let or const" --> ".event"
13."Set onClick method" --> ".click"
14."Set mouseOver method" --> ".hover"

## include in your javascript.json file:
```
"Arrow function with params": {
	"prefix": "afunp",
	"body": [
		"const ${1:name} = (${2:params}) => {",
		"   ${3://content}",
		"};",
		"$0"
	],
	"description": "Arrow function with params"
},
"Arrow function without params": {
	"prefix": "afun",
	"body": [
		"const ${1:name} = () => {",
		"   ${2:params}",
		"};",
		"$0"
	],
	"description": "Arrow function without params"
},
"Show an item list": {
	"prefix": "rvc",
	"body": [
		"document.addEventListener('DOMContentLoaded', () => {",
		"   ${1:funcName}();",
		"});",
		"",
		"let ${2:object}List = [",
		"   {",
		"      id: 0,",
		"      key: 'value',",
		"   },",
		"];",
		"",
		"const ${1:funcName} = () => {",
		"   let view = '';",
		"   ${2:object}List.forEach(${2:object} => {",
		"      view = view + `",
		"         <li>",
		"            ${4://li item}",
		"         </li>",
		"      `;",
		"   });",
		"   document.querySelector('${3:identifier}').innerHTML = view;",
		"}",
		"$0"
	],
	"description": "Show an item list"
},
"Create html element from JavaScript": {
	"prefix": "create",
	"body": [
		"const ${1:element} = `",
		"",
		"   ${4://put html...}",
		"",
		"`;",
		"const ${3:name} = document.querySelector('${2:identifier}');",
		"${3:name}.innerHTML = ${1:element};",
		"${0}"
	],
	"description": "Create an html element"
},
"Array list with an object": {
	"prefix": "arr",
	"body": [
		"let ${1:name}List = [",
		"   {",
		"      id: 0,",
		"      ${2:key}: ${3:value},",
		"   }",
		"];",
		"$0"
	],
	"description": "Arraylist with an object"
},
"Array list object": {
	"prefix": "arro",
	"body": [
		",",
		"{",
		"   id: ${1:index},",
		"   ${2:key}: ${3:value},",
		"}"
	],
	"description": "Put a new arrayList object"
},
"Call function": {
	"prefix": "callf",
	"body": [
		"${1:name}(${2:params});",
		"${0}"
	],
	"description": "Call function with params"
},
"Get view in const or let": {
	"prefix": "getv",
	"body": [
		"document.querySelector('${1:container}')${2:;}",
		"${0}"
	],
	"description": "Get view in const or let"
},
"Call and get view in let": {
	"prefix": "getvl",
	"body": [
		"let ${1:name} = document.querySelector('${2:container}')${3:;}",
		"${0}"
	],
	"description": "Call view and save it in let"
},
"Call and get view in const": {
	"prefix": "getvc",
	"body": [
		"const ${1:name} = document.querySelector('${2:container}')${3:;}",
		"${0}"
	],
	"description": "Call view and save it in const"
},
"Call view and set eventListener": {
	"prefix": "getve",
	"body": [
		"document.querySelector('${1:container}').addEventListener('${2:event}', () => {",
		"   ${3://do something...}",
		"});",
		"${0}"
	],
	"description": "Call view and set eventListener"
},
"Set eventListener on let or const": {
	"prefix": ".event",
	"body": [
		".addEventListener('${1:event}', () => {",
		"   ${2://do something...}",
		"});",
		"${0}"
	],
	"description": "Set eventListener on let or const"
},
"Set onClick method": {
	"prefix": ".click",
	"body": [
		".addEventListener('click', () => {",
		"   ${1://do something...}",
		"});",
		"${0}"
	],
	"description": "Set onClick method"
},
"Set mouseOver method": {
	"prefix": ".hover",
	"body": [
		".addEventListener('mouseover', () => {",
		"   ${1://do something...}",
		"});",
		"${0}"
	],
	"description": "Set mouseOver method"
}
```
