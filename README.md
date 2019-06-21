# A-frame Trackball Controls component

[![License](http://img.shields.io/npm/l/aframe-stl-exporter-component.svg?style=flat-square)](https://npmjs.org/package/aframe-stl-exporter-component)

A Trackball Controls component for [A-Frame](https://aframe.io).

### API

| Property | Description | Default Value |
| -------- | ----------- | ------------- |
| rotateSpeed  | Number – rotation speed | 1 |

### Installation

#### Browser

Install and use by directly including the [browser files](dist):
```html
<head>
  <title>A-Frame using a Camera with Trackball Controls</title>
  <script src="https://aframe.io/releases/0.9.2/aframe.min.js"></script>
  <script src="./aframe-trackball-controls-component.min.js"></script>
</head>

<body>
  <a-scene>
    <a-entity
          id="camera"
          camera="fov: 80; zoom: 1;"
          position="0 1.65 5"
          trackball-controls="
              rotateSpeed: 1.0;
              zoomSpeed: 1.2;
              panSpeed: 0.8;
              noZoom: false;
              noPan: false;
              staticMoving: true;
              dynamicDampingFactor: 0.3;
              "
          mouse-cursor="">
          <a-entity geometry="primitive:cone; radius-bottom:1; radius-top:0" scale=".33 1 .33" position="0 0 0" rotation="90 0 0" material="color: #0099ff; transparent: true; opacity:0.5"></a-entity>
      </a-entity>

      <a-entity id="target">
          <a-box id="box" position="-1 0.5 1" rotation="0 45 0" color="#4CC3D9"></a-box>
          <a-sphere id="sphere" position="0 1.25 -1" radius="1.25" color="#EF2D5E"></a-sphere>
          <a-cylinder id="cylinder" position="1 0.75 1" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
          <a-plane position="0 0 0" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
      </a-entity>

      <a-sky color="#ECECEC"></a-sky>
  </a-scene>
</body>
```

More information about the component and its options could be found on the [three.js Trackball Controls](https://threejs.org/examples/#misc_controls_trackball)

#### npm

Install via npm:
