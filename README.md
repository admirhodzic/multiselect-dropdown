# multiselect-dropdown
Pure JavaScript, no dependencies, dropdown list with multiselect capability.

![Sample screenshot](demo.png)
## Installation
Include multiselect-dropdown.js in your HTML.

    <script src="multiselect-dropdown.js" ></script>

## Usage
Just add "multiple" attribute to SELECT elements.
    
    <select multiple id="sel1"> 
        ... 
    </select>

To enable dynamic list search, add multiselect-search="true" attribute.

    <select multiple id="sel1" multiselect-search="true"> 
        ... 
    </select>

To update options list, call *selectId.loadOptions()* where "selectId" is HTML select element.

    fetch("/options").then(d=>d.json()).then(d=>{
      sel1.innerHTML = 
        d.map(t=>'<option value="'+t.value+'">'+t.text+'</option>');

      sel1.loadOptions();
    })



## Demo

[Demo Page](https://admirhodzic.github.io/multiselect-dropdown/demo.html)
