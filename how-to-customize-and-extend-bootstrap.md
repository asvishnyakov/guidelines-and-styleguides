# How to customize and extend bootstrap

## About terms

> **Customization** - The action of modifying something to suit a particular individual or task.

> **Extensibility** - The quality of being designed to allow the addition of new capabilities or functionality.

\- [Oxford Dictionary](https://www.lexico.com/)

## Bootstrap customization

## Bootstrap extensibility

### Encapsulate component-specific code into special classes or use framework possibilities

#### Do

If you need to changes styles specific for some components or situations, like adding spacing before icon, then always incapsulate these changes into specific classes, i.e.:
```scss
.category-page {
  .btn .fa {
    margin-left: $icon-space;
  }
}
```

#### Why?

If you will use global styles for this without encapsulation, these styles will be implemented across all applicable elements on site:

```scss
.btn .fa {
  margin-left: 5px;
}
```

#### How problem resolved in frameworks?

Frameworks like Angular use [Shadow DOM](https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_shadow_DOM) to [encapsulate](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)) styles, i.e. isolate styles from component to prevent their affection of global styles or another component styles.

#### Citations:

> Components should be built with a base class and extended via modifier classes

> An important aspect of web components is encapsulation — being able to keep the markup structure, style, and behavior hidden and separate from other code on the page so that different parts do not clash, and the code can be kept nice and clean.

#### Links:

* https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#Specificity
* https://getbootstrap.com/docs/4.5/extend/approach/#classes
* https://angular.io/guide/component-styles#view-encapsulation