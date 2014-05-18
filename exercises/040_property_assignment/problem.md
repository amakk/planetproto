Property Assignments
-----------------------

What happens if you update a property that already exists in the prototype? Let's see:

```js
	var person = {
		kind: 'person'
	}

	var zack = {}
	zack.__proto__ = person

	zack.kind = 'zack'

	console.log(zack.kind); //=> 'zack'
	// zack now has a 'kind' property

	console.log(person.kind); //=> 'person'
	// person has not being modified
```

New / updated properties are assigned to the object, not to the prototype
Note that the property 'kind' now exists in both person and zack.

Challenge
---------

Make a program that
- Defines three objects: 'animal', 'cat' and 'dog'
- In the definition of animal adds a property 'legs' set to null.
- Makes animal the prototype of cat and dog
- Asserts animals.legs, cat.legs and dog.legs (in that order)
- Sets cat.legs to 4 by direct assignment
- Asserts again animals.legs, cat.legs and dog.legs (in that order)

Boilerplate
-----------

```js
var assert = require('assert');
... you code here ...

module.exports = {
	animal: animal,
	dog:    dog,
	cat:    cat
}
```