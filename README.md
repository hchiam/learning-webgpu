# Learning WebGPU

Just one of the things I'm learning. https://github.com/hchiam/learning

(Compare with the older WebGL: https://github.com/hchiam/learning-webgl)

To enable WebGPU in Chrome now: chrome://flags/#enable-webgpu-developer-features

https://caniuse.com/webgpu

https://codelabs.developers.google.com/your-first-webgpu-app#0

https://glitch.com/edit/#!/your-first-webgpu-app

https://your-first-webgpu-app.glitch.me/

gpu --> adapter --> device --> canvas format and context config --> encoder

```js
const adapter = await navigator.gpu?.requestAdapter();
const device = await adapter?.requestDevice();
const canvasFormat = navigator.gpu?.getPreferredCanvasFormat();
canvas.getContext("...").configure({
  device: device,
  format: canvasFormat,
});
const encoder = device?.createCommandEncoder();
// encoder.beginRenderPass
// context.getCurrentTexture
```
