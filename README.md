# Bootstrap Tree View

forked from https://github.com/jonmiles/bootstrap-treeview

## a list of changes

In order to make it meet my requirements, the following methods has been added.

### filter

a method for node filtering

parameter:

* func: the filter function, like Array.filter

```js
// filter nodes by a function
// useful when need to find node by attribute
var nodes = $('#treeview').treeview("filter", function (node) {
	return (node.id == 3);
});
```

### addNode

dynamic add a node

parameter:

* parentNodeId: parent node id
* node: node object

```javascript
var nodes = $('#treeview').treeview("getSelected");
var nodeId = nodes.length ? nodes[0].nodeId: null;
$('#treeview').treeview("addNode", [nodeId, {
  text: 'i am a new node!!!',
  id: 9999                   
}]);
```

## Demostration

public/example.html

## Copyright and Licensing
Copyright 2013 Jonathan Miles

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at <http://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
