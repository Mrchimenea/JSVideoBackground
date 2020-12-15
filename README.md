# JSVideoBackground

A responsive video background function in javascript which resizes with the container.

## Installation

Include **JSVideoBackground.js** with a script tag:

```html
<script type="text/javascript" src="JSVideoBackground.js"></script>
```

## Usage

Your must have a HTML container element with a video tag inside, for example:

```html
<div id="video-container" style="width: 100%; min-height: 100vh">

<video id="video">
<source src="video.mp4" type="video/mp4">
</video> 

<div>
I am an element on the video background.
</div>

</div>
```

Then you can call JSVideoBackground function like this:

```html
<script type="text/javascript">

(function() {

    var video = document.getElementById("video");
    var container = document.getElementById("video-container");
    var options = {
      responsive: true,
      mobilevideo: "light-video.mp4",
    };

    JSVideoBackground(video, options, container);

})();

</script>
```

## Parametres

For JSVideoBackground(), video object is required, options and container are optional. If no container is defined it will be used the the video tag parent element.

## Options

Resize video background with the container:

**responsive:** (boolean) default true.

Load a different video source by detecting mobile devices [(supported devices in detectmobilebrowsers.com)](http://detectmobilebrowsers.com):

**mobilevideo:** (URL) default null.

Some video tag attributes are predefined, you can change them using following options:

**autoplay:** (boolean) default true.

**loop:** (boolean) default true.

**controls:** (boolean) default false.

**muted:** (boolean) default true.

Check [video tag documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video) for more information. 

## License

License under [MIT](https://choosealicense.com/licenses/mit/)