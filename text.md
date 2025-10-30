<!-- include A-Frame obviously -->
<script src="https://aframe.io/releases/0.6.0/aframe.min.js"></script>
<!-- include ar.js for A-Frame -->
<script src="https://jeromeetienne.github.io/AR.js/aframe/build/aframe-ar.js"></script>
<body style='margin : 0px; overflow: hidden;'>
  <a-scene embedded arjs>
      <!-- Pré-carregamento de ativos -->
      <a-assets>
        <!-- Caminho relativo do modelo GLB -->
        <a-asset-item id="glbModel" src="cadeiras.glb"></a-asset-item>
      </a-assets>
            <!-- Modelo 3D -->
      <a-gltf-model
        src="#glbModel"
        position="0 0 -3"
        scale="1 1 1"
        rotation="0 180 0"
      ></a-gltf-model>
    <!-- create your content here. just a box for now 
    <a-box position='0 0.5 0' material='opacity: 0.5;'></a-box> -->
    <!-- define a camera which will move according to the marker position -->
    <a-marker-camera preset='hiro'></a-marker-camera>
  </a-scene>
</body>



---------------
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Teste Aula Bicho</title>

    <!-- Biblioteca A-Frame -->
    <script src="https://aframe.io/releases/1.7.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <!-- Pré-carregamento de ativos -->
      <a-assets>
        <!-- Caminho relativo do modelo GLB -->
        <a-asset-item id="glbModel" src="cadeiras.glb"></a-asset-item>
      </a-assets>

      <!-- Modelo 3D -->
      <a-gltf-model
        src="#glbModel"
        position="0 0 -3"
        scale="1 1 1"
        rotation="0 180 0"
      ></a-gltf-model>

      <!-- Adicionando câmera e luz para visualização adequada -->
      <a-entity light="type: ambient; color: #ffffff; intensity: 0.8"></a-entity>
      <a-entity light="type: directional; color: #ffffff; intensity: 0.6" position="1 1 1"></a-entity>
      <!-- <a-entity camera position="0 1.6 0"></a-entity> -->
    </a-scene>
  </body>
</html>
