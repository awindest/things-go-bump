<script lang="ts">
  import { Canvas, extend } from '@threlte/core'
  import Scene from './Scene.svelte'
  import * as THREE from 'three/webgpu'

  extend(THREE)
</script>

<div>
  <Canvas
    createRenderer={(canvas) => {
      return new THREE.WebGPURenderer({
        canvas,
        antialias: true,
        forceWebGL: false
      })
    }}
  >
    <Scene />
  </Canvas>
</div>

<style>
  div {
    position: absolute;
    height: 100%;
    width: 100%;
  }
</style>
