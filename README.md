# Things to watch out for in the Polymer 2 upgrade

## Sass
Nesting will not work with the `:host` or `:slotted` pseudo-classes.

This won't work:
```
:host {
  &[full-bleed] .content {
    padding: 0;
  }
}
```
Do this instead:
```
:host([full-bleed]) .content {
  padding: 0;
}
```

## Import Paths
If you see 404s when loading local assets in Polymer 2.x:

`<img src="[[importPath]]monogram-wdmk.png"`
[see Polymer docs](https://www.polymer-project.org/2.0/docs/devguide/dom-template#urls-in-templates)
