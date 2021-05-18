# aframe-websurfaces

An [aframe](https://github.com/aframevr/aframe) component for adding interactable web pages to your scene.

![Example gif](https://github.com/ryota-mitarai/aframe-websurfaces/blob/master/examples/example1.gif)

## Usage

To create a websurface, just add the **websurface** component. This will create an iframe and project it's contents onto a plane:

```html
<a-entity websurface></a-entity>
```

### Properties

| Property         | Description                               | Default             |
| ---------------- | ----------------------------------------- | ------------------- |
| url              | the url of the web page                   | "https://aframe.io" |
| width            | width of the websurface                   | 1                   |
| height           | height of the websurface                  | 0.75                |
|                  |                                           |
| frameSkips       | updates render\* on every n cycles        | 1                   |
| autoSceneStyling | sets _scene.style.position_ to "absolute" | true                |

\*note - only the shape of the web page in the scene is affected by this, the web page will still play at normal speed

## Additional Info

The web page is not actually present inside the aframe scene, only an empty plane is. Because of this, the web page is not visible in VR.

Under the hood this uses a modified version of [three-dom-elements](https://github.com/CodyJasonBennett/three-dom-elements), massive props there.
