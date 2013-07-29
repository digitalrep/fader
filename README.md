DigitalRepInfo Jquery Fader
===========================

Included Files:
---------------
<table>
  <tr><th>Description</th><th>File</th></tr>
  <tr><td>Example usage:</td><td>example.htm</td></tr>
  <tr><td>CSS:</td><td>css/fader.css</td></tr>
  <tr><td>Javascript:</td><td>js/fader.js</td></tr>
  <tr><td>Left Image:</td><td>fader_images/fader_left.png</td></tr>
  <tr><td>Left Image (Over):</td><td>fader_ images/fader_left2.png</td></tr>
  <tr><td>Right Image:</td><td>fader_images/fader_right.png</td></tr>
  <tr><td>Right Image (Over):</td><td>fader_images/fader_right2.png</td></tr>
  <tr><td>Fader Images:</td><td>images/</td></tr>
</table>

How to use it:
--------------

Unzip the files to your htdocs folder on your web server. 

Inside your html document, in the head section, include the css file (before the javascript):
```
<link rel="stylesheet" type="text/css" media="screen" href="css/fader.css" />
```
Next, inside your html document's head section, include the jquery javascript source file:
```
<script type="text/javascript" src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script> 
```
Also include the fader javascript source file: 
```
<script type="text/javascript" src="js/fader.js"></script> 
```
Include this code next, and put your own values in to specify options: 
```
<script type="text/javascript">
$(function()
{
    var fader_properties = 
    {
        autoplay: true, 
        auto_speed: 5000,
        fade_speed: 500,
        width: 640,
        height: 424
    };
    $('#fader').begin(fader_properties);
});
</script> 
```
Note that:
----------

- Autoplay can be true or false, depending on whether you want the fader to autoplay
- Auto_speed is the speed at which the image changes during autoplay; note that 5000 = 5 seconds
- Fade_speed is the speed at which the images fade in/out; 500 = half a second
- Width is the width of the fader; the images inside the fader will be this width
- Height is the height of the fader; the images inside the fader will be of slightly less tall than this

Finally, in your html, include this code:
-----------------------------------------
```
<div id="fader">
    <div id="fader_img">
        <img src="images/Penguins.jpg">
        <img src="images/Lighthouse.jpg">
        <img src="images/Tulips.jpg">
    </div>
    <div id="fader_left">
        <a href="#">
            <img src="fader_images/fader_left.png" id="sl">
            <img src="fader_images/fader_left2.png" id="sl2">
        </a>
    </div>
    <div id="fader_bips">
    </div>
    <div id="fader_right">
        <a href="#">
            <img src="fader_images/fader_right.png" id="sr">
            <img src="fader_images/fader_right2.png" id="sr2">
        </a>
    </div>
</div>
```
Note that:
----------

Replace the contents of div#fader_img with the locations of the images you want to display in the fader

Supported Browsers:
-------------------

Works in Internet Explorer 9 & 10, Chrome 27.0.1453.110 m, Firefox 21.0, and Safari 5.1.7. 
To support older versions of Internet Explorer, consider using html5shiv.js.