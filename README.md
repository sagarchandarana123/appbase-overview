# Appbase Overview

## Objects and Properties

An _object_ in Appbase very similar to a JSON object, and contains key/value pairs. The keys in an object are called the _properties_ of the _object_. An object can be created using `Appbase.new({pk: key})`, where the `key` is a _primary key_ given to the object, and this key can be used later on to _fetch_ the object from Appbase. If no `key` is given, a random string will be assigned as the key for the object. `Appbase.new()` returns an `Appbase Reference Object` which is a reference to the object stored in Appbase. Read/write operations can be carried out this reference object.

Properties can be accessed using __TODO__ method and they can only contain primitive data (Number/String). To set value for a property, use __TODO__ method.

Example:
```javascript
TODO
```

## Namespaces

Every object belongs to a _namespace_. Namespaces can be used to categorize the _types_ of objects. For eg., in a chat application, the namespaces could be: `User, Chat, ChatGroup` etc. 

Namespace are __NOT__ containers of objects, and the _primary key_ of an object is unique across all the namespaces. Namespaces are there to categorize objects. This categorization helps applying security rules on objects which are alike, and should be treated much the same. For eg., the objects of the `ChatGroup`, must only be visible to the members of the chat group. Such a rule can be imposed on the namespace and all the objects in that namespace would follow the rule. 

`Appbase.new({ns: namespace, pk: key})` method creates objects in the given `namespace`, and if no namespace is specified, the objects goto into the namespace called __Default__. 

Namespaces are automatically created when a new namespace is specified in `Appbase.new()`, although this behavior can be controlled by security rules. An object can be moved amongst namespaces, which might be useful over the course of development. 

To access an object which was previously created using `Appbase.new()`, use `Appbase.ref(namespace/key)`, which returns an Appbase Reference to the object.

Example:
```javascript
TODO
```

## The Graph

Today's application are complex and the objects in the application are linked to eachother in a number of ways and dimensions. For eg., social applications. The data of such applications can not be modelled in a simple Table-Row or Tree data structure.

### Links

In _Appbase_ a number of links can be pointed from one object to other objects, allowing you to create a _Graph_. Links in an object are _named_ and _ordered_. 

### Paths

## Realtime




