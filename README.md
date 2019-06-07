# Object
对象相关操作


Object每个实例都有以下几种方法：
  constructer、hasOwnProperty()、isPrototypeOf、propertyIsEnumerable()、toString()、toLocateString()、valueOf()
  原型.isPrototype(obj)：用于检查传入的对象是否是当前对象的原型,同intanceof一个效果，只要在原型链上出现过的原型，都可以说是该原型链所派生的实例的原型。
  propertyIsEnumerable(propertyName)：用于检查给定的属性是否能够用for-in语句来枚举。

Object构造函数的方法：
  Object.defineProperty():自定义对象属性的内部特性，用这个方法默认都是false
  Object.getOwnPropertyNames(prop):得到所有实例属性,包括实例属性和原型属性
  Object.getOwnPropertyDescriptor(obj, prop) 方法返回指定对象上一个自有属性对应的属性描述符。实例属性包括两种：数据属性和可访问属性

in操作符：有两种方式单独使用和for...in使用。in操作符会在无论在实例中还是原型中该对象能访问的属性都返回true。而for...in中使用，返回的是无论在实例中还是原型中该对象能够通过对象访问的可枚举的属性。
要取得对象上所有可枚举的实例属性可以用Object.keys()方法，注意只是实例属性不包括其原型上的属性。如果你想得到所有实例属性，可以通过Object.getOwnPropertyNames()方法,这两个方法都可以替代for...in循环
