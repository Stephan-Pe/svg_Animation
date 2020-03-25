# SVG Animation
Author: Stephan Petersen
E-Mail: st.petersen63@gmail.com

## Create your Signature as an SVG Animation

- First of all you will need an Graphic App like Vectornator to create the SVG
- Export the file so that you can work with it
-  you maybe have code like following inside your SVG

```html
<path d="M5466.83,1530.44c33.709,-146.192 249.625,-75.771 360.167,-126.45c145.083,-66.484 182.042,-159.996 237.583,-298.875" style="fill:none;stroke:#ff0000;stroke-width:70.13px;"/>
```
- for the animation you need a stroke so you can change it like this
```html
<path stroke="#ff0000" stroke-width="70.13px" d="M5466.83,1530.44c33.709,-146.192 249.625,-75.771 360.167,-126.45c145.083,-66.484 182.042,-159.996 237.583,-298.875" style="fill:none;"/>
```
- then you can add different classes to it and find out the lenght of the stroke with a console.log();

```js
var path = document.querySelector('.mrAt');
var length = path.getTotalLength();

console.log(length);
```
- for your Signature or the text you want to write you may have more than one stroke, so you have to work on the timing of your animations
```css
.mrAt {
  stroke-dasharray: 8255;
  stroke-dashoffset: 8255;
  animation: ipoint 700ms linear 3250ms forwards;
}
@keyframes ipoint {
  from {
      stroke-dashoffset: 8255;
  }
  to {
      stroke-dashoffset: 0;
  }

}
```
### Good Luck and have fun! ;-)




