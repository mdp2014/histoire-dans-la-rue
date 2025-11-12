# Histoire dans la rue

Ce dépôt contient le projet « histoire-dans-la-rue ». Structure minimale générée automatiquement : un dossier `src/`, un `README.md` (en français), un fichier `.gitignore` et une licence MIT.

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)

## But

Projet de démonstration/point de départ pour développer une application liée aux histoires de rue (site web, API ou script). Personnalise selon tes besoins.

## Visualisation du projet

### Animation interactive
<div style="width: 100px; height: 100px; background-color: red; animation: move 2s infinite;">
  <script>
    document.querySelector('div').addEventListener('click', function() {
      alert('Clicked!');
    });
  </script>
</div>

<style>
  @keyframes move {
    0% { transform: translateX(0); }
    50% { transform: translateX(100px); }
    100% { transform: translateX(0); }
  }
</style>

### Animation 3D
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<div id="threejs-container" style="width: 200px; height: 200px;"></div>
<script>
  var scene = new THREE.Scene();
  var camera = new THREE.PerspectiveCamera(75, 1, 0.1, 1000);
  var renderer = new THREE.WebGLRenderer();
  renderer.setSize(200, 200);
  document.getElementById('threejs-container').appendChild(renderer.domElement);

  var geometry = new THREE.BoxGeometry();
  var material = new THREE.MeshBasicMaterial({ color: 0x00ff00 });
  var cube = new THREE.Mesh(geometry, material);
  scene.add(cube);

  camera.position.z = 5;

  function animate() {
    requestAnimationFrame(animate);
    cube.rotation.x += 0.01;
    cube.rotation.y += 0.01;
    renderer.render(scene, camera);
  }

  animate();
</script>

### Animation GIF
![Animation](https://media.giphy.com/media/3o7TKSjRrfIPjeiVyE/giphy.gif)

## Contenu généré

- `src/` : dossier source (vide pour l'instant)
- `README.md` : ce fichier
- `.gitignore` : patterns génériques
- `LICENSE` : licence MIT

## Essayer rapidement

1. Ouvre le dossier dans VS Code :


