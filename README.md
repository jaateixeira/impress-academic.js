# Impress-academic.js

collection of styles (css) and scripts (js) that leverage the impress.js for more academic presentations

impress.js | presentation tool based on the power of CSS3 transforms and transitions in modern browsers | by Bartek Szopka @bartaz

This stiles and scripts help you to make academic presentations on top of it.

* Suport for references lists
* Stiles that focus more on content
* Style for pictures that take all the screen
* A dynamic timer that allows to see how long are you taking 

# Dependencies 

Impress-academic.js is nothing without [impress.js](https://impress.js.org/). 


# How to use it for HTML/CSS/JS based presentations 

- First, you must clone the impress.js project
```
git clone https://github.com/impress/impress.js.git
 ```  
- Then clone the Impress-academic.js
```
git clone https://github.com/jaateixeira/impress-academic.js.git
```

- The impress-academic-common.css with the defined classes is now avilable
- See [http://users.abo.fi/jteixeir/presentations/trial-lecture-16th-may/](http://users.abo.fi/jteixeir/presentations/trial-lecture-16th-may/) for a example on how to use it.

You impress.js presentation must the include 
```html 
	<link href="./impress-academic.js/css/impress-academic-common.css" rel="stylesheet" />
```

# Minimal example with **impress.js** and **impress-academic.js**

```html
<!doctype html>

<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=1024" />
    <meta name="apple-mobile-web-app-capable" content="yes" />
    <title> Hello </title>

    <meta name="description" content="Hello" />
    <meta name="author" content="apolinex the great" />



    <link rel="preconnect" href="https://fonts.googleapis.com">
	 <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

	 <link href="//fonts.googleapis.com/css?family=Open+Sans:regular,semibold,italic,italicsemibold|PT+Sans:400,700,400italic,700italic|PT+Serif:400,700,400italic,700italic" rel="stylesheet" />
	 <link href="https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap" rel="stylesheet">




    <link href="./impress.js/css/impress-demo.css" rel="stylesheet" />
    <link href="./impress.js/css/impress-common.css" rel="stylesheet" />

	<link href="./impress-academic.js/css/impress-academic-common.css" rel="stylesheet" />

	 <!-- for the timer -->
	 <link rel="stylesheet" href="./impress-academic.js/timer-src/styles.css">

</head>


<body class="impress-not-supported">

<!--
    For example this fallback message is only visible when there is `impress-not-supported` class on body.
-->
<div class="fallback-message">
    <p>Your browser <b>doesn't support the features required</b> by impress.js, so you are presented with a simplified version of this presentation.</p>
    <p>For the best experience please use the latest <b>Chrome</b>, <b>Safari</b> or <b>Firefox</b> browser.</p>
</div>

<div id="impress"
    data-transition-duration="1000"

    data-width="1024"
    data-height="768"
    data-max-scale="3"
    data-min-scale="0"
    data-perspective="1000"

    data-autoplay="0">

    <div id="Intro" class="step slide" data-x="0" data-y="-1000">



          <h2 class="quote">
            Hello world
          </h2>

    </div>

    <div id="overview" class="step" data-x="4000" data-y="2000" data-z="0" data-scale="10">
    </div>

</div>



<div id="impress-toolbar" style=" position: absolute;
  right: 20px;
  width: 550px;
  bottom: 10px;">
</div>



<div class="impress-progress" style="position:absolute;
left:20px;
width:100px;
bottom:10px;"></div>



<div class="impress-progressbar"></div>



<div id="app"></div>
<script src="./impress-academic.js/timer-src/index.js">

<div class="hint">
    <p>Use a spacebar or arrow keys to navigate. <br/>
       Press 'P' to launch speaker console.</p>
</div>
<script>
if ("ontouchstart" in document.documentElement) {
    document.querySelector(".hint").innerHTML = "<p>Swipe left or right to navigate</p>";
}
</script>


<script src="impress.js/js/impress.js"></script>
<script>impress().init();</script>

<script src="impress.js/js/impressConsole.js"></script>



</body>
</html>


```
