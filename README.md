# minimit-gallery

**Minimit Gallery is a custom slider plugin. It supports drags, scrollers, touch interactions, hash and
pushstate links.**

It is a library agnostic javascript plugin, built for advanced frontend developers, who wants to spend less time coding the logic, and more time coding the animations.

It’s very customizable, but you have to code the animation, all the css, and some of the logic of the slider.
To understand how to use this plugin see the [2.0 guide](http://www.minimit.com/articles/code-tips/minimit-gallery-2-0-guide) and the demo page.

#### Browser support
IE7+, Firefox 3.5+, Safari 3+, Chrome, Ios, Android.

#### [Guide](http://www.minimit.com/articles/code-tips/minimit-gallery-2-0-guide)

My website [minimit.com](http://www.minimit.com) and my [twitter](http://twitter.com/beaver82minimit).


Alert
-------
This is still an experimental plugin, with an API subject to change in the future. If you have new ideas how to make the code simpler and with fewer settings, please drop me a line.

Usage
-----
``` html
<!-- specify the html items -->
<div id="reference-item-0">0</div>
<div id="reference-item-1">1</div>
<div id="reference-item-2">2</div>
<div id="reference-item-3">3</div>
<div id="reference-item-4">4</div>
<div id="reference-item-5">5</div>

<!-- include mg Javascript code -->
<script type="text/javascript" src="mg.min.js"></script>

<script type="text/javascript">
// construct gallery
var mgObject = new Mg({
    reference:"reference",
    click:{
        activated:[0],
        cycle:true,
        interactive:true,
        maxActivated:1,
        auto:1000, autoSlow:5000
    }
});

// specify gallery click event function
mgObject.click.onEvent = function(){
    document.getElementById("#"+this.reference+"-item-"+this.deactivated).className = '';
    document.getElementById("#"+this.reference+"-item-"+this.activated).className = 'active';
}

// init the gallery
mgObject.init();
</script>
```

Acknowledgements
-------
Copyright © 2013 Riccardo Caroli. Licensed under [MIT license](http://www.opensource.org/licenses/mit-license.php).
