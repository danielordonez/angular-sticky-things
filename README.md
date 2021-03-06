[![npm version](https://badge.fury.io/js/%40w11k%2Fangular-sticky-things.svg)](https://badge.fury.io/js/%40w11k%2Fangular-sticky-things)

# Angular Sticky Things

A pure TypeScript directive for making things sticky when the user scrolls (for Angular 2+).

[See the demo here](https://w11k.github.io/angular-sticky-things/).


### Requirements

* Angular (requires Angular 4.x or higher)
* Supports all major browsers and IE9 and up (lower versions might not be supported)

### Features:
* Stick all the things!
* Super smooth!
* Tested in real world projects
* Support for Angular Universal
* Prevents page-jumping when switching to sticky mode
* No jQuery or other dependencies - pure Angular solution

### Installation

with npm:
```
npm install @w11k/angular-sticky-things
```

with yarn:
```
yarn add @w11k/angular-sticky-things
```


Now import the **AngularStickyThingsModule** in the corresponding Module
```
import {AngularStickyThingsModule} from '@w11k/angular-sticky-things';

@NgModule({
  declarations: [
  ],
  imports: [
    AngularStickyThingsModule,
  ],
  providers: [],
})
export class SomeModule { }
```


### Usage:
```html
<div #spacer></div>
<div stickyThing [spacer]="spacer">
  I am sticky!
</div>
```


#### Boundary Elements

If a boundary element is defined, the sticky element scrolls only within the height of the boundary element and then stops. This is useful if you have multiple sticky elements since it prevents stacking. You can [take a look at the examples](https://w11k.github.io/angular-sticky-things/).
```html
<div #boundary style="height:1000px;">
  <div #spacer></div>
  <div stickyThing [spacer]="spacer" [boundary]="boundary">
    I am sticky but only inside #boundary!
  </div>
</div>

```

*Hint*: The boundary feature is still in beta - position errors might occur!

#### Spacer

The spacer is not required but prevents a page jump when the sticky effect steps in.

## Patron

❤️ [W11K - The Web Engineers](https://www.w11k.de/)

❤️ [theCodeCampus - Trainings for Angular and TypeScript](https://www.thecodecampus.de/)
