# Using vuejs with aframe

Aframe is great, vuejs is great why not combine them?

This demo uses a custom vue component to wrap an aframe entity to add reactive magic to the aframe scene
https://rawgit.com/frederic-schwarz/aframe-vuejs-3dio/master/index.html

## Basic setup:
custom component with reactive property within the aframe scene
```html
<a-scene>
  <my-component :furniture-id="id"></my-component>
</a-scene>
```
vue.js component definition
```js
Vue.component('my-component', {
  props: ['furnitureId'],
  template: `<a-entity :io3d-furniture="'id:' + furnitureId"></a-entity>`
})    
```

Take a look at `index.html` for the actual implementation.

Result:

![Find furniture](https://storage.3d.io/97fa0bf7-1405-4fe3-a2be-49d2101d4121/2017-09-19_07-43-20_BbtYrY/vue-furniture.gif)

furniture via [3d.io](https://3d.io/docs/api/1/furniture.html)
