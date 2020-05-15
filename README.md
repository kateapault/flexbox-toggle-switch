# Toggle Switch

This is a pure CSS/HTML toggle switch (or toggle button, or toggle bar - whatever your preference is) using Flexbox. 

I was looking for a toggle switch and found a pre-flexbox CSS/HTML template for one, plus a few with JS - I was trying to put this into a React app so I didn't want to start adding vanilla JS, and making any tweaks to the pre-flexbox CSS messed with what I already had for the site. So I made my own!

![example toggles](https://github.com/kateapault/flexbox-toggle-switch/blob/master/assets/Example.png?raw=true)

# Simple Round Toggle
<br>
<b>HTML</b>
<br>


```html
<input type="checkbox" id="optionA"/>
<label for="optionA" class="toggle">
  <div class="slider"></div>
</label>
```

<b>CSS</b>
<br>
```
.toggle {
    background-color: grey;
    width: 60px;
    height: 32px;
    border-radius: 16px;
    display: flex;
    flex-direction: column;
  }
  
input {
  display: none;
}
  
.slider {
  height: 24px;
  width: 24px;
  background-color: white;
  border-radius: 12px;
  margin: 4px;
}

input:checked + .toggle {
  background-color: green;
}
  
input:checked + .toggle > .slider {
  align-self: flex-end;
}
  
```

# Simple Square Toggle
<i>Basically the same, just without the border-radius attribute in CSS. It's written here for copy/paste convenience though:</i>
<br>
<br>
<b>HTML</b>
<br>


```html
<input type="checkbox" id="optionA"/>
<label for="optionA" class="toggle">
  <div class="slider"></div>
</label>
```

<b>CSS</b>
<br>
```
.toggle {
    background-color: grey;
    width: 60px;
    height: 32px;
    display: flex;
    flex-direction: column;
  }
  
input {
  display: none;
}
  
.slider {
  height: 24px;
  width: 24px;
  background-color: white;
  margin: 4px;
}

input:checked + .toggle {
  background-color: green;
}
  
input:checked + .toggle > .slider {
  align-self: flex-end;
}
  
```
