three-software-renderer
=======================
##Universal Three.js in-memory renderer for node.js and the browser

# What's this for?
The `SoftwareRenderer` is a drop-in renderer for [Three.js](http://www.three.js.org) that can be used on the server and the client,
if you need to be GPU independent.

# What's the drawback?
Primarily performance. As this renderer does not have access to GPU acceleration and GPU shader units, it's much much slower than the CanvasRenderer or WebGLRenderer.
In addition, you'll have to use `THREE.DataTexture` instead of a normal `THREE.Texture` for textures when you're in a headless environment (i.e. node.js).

# What are possible use cases?
* Rendering in a web worker, e.g. for static renderings that should happen in the background
* Rendering on the server, e.g. for preview images of 3D models
* Tell me, if you have other ideas

# Which Three.js version is this compatible with?
So far I have tested 0.69 and 0.71. Please tell me if you tried it with other versions as well :-)

# What is this work based on?
First and foremost this is just a modified copy of the SoftwareRenderer found in [the Three.js example sources](https://github.com/mrdoob/three.js/blob/0b07813dc45481f1d16d3b6d2334178664861465/examples/js/renderers/SoftwareRenderer.js).
It also uses the modified [THREE.Projector](https://github.com/mrdoob/three.js/blob/20b77b2785afaa4d00a1ecd222e6de1a3ec76006/examples/js/renderers/Projector.js) from the examples.

# I found a bug, how can I help?
Please help me improve this module by opening an issue on Github. If you have an idea what might cause the problem, I'd be very grateful if you'd try to investigate the bug and make a pull request to this repository.
If you have any questions or need help doing so, let me know via the issues in this project!
