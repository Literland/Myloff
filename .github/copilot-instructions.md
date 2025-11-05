# Guía para Agentes AI - Mytaekook

Este documento proporciona información esencial para que los agentes AI trabajen efectivamente en este proyecto.

## Arquitectura y Estructura

Este es un proyecto web interactivo que implementa una galería de fotos multimedia con las siguientes características clave:

- Sistema de escenas múltiples con transiciones suaves
- Modo 3D inmersivo con efectos parallax
- Manejo avanzado de multimedia (audio e imágenes)
- Interacciones táctiles y de arrastre
- Efectos visuales dinámicos (partículas, corazones, estrellas)

### Componentes Principales

- **Sistema de Escenas**: Maneja 4 escenas temáticas (Jardín de Nieve, Universo, Hogar, Galería)
- **Sistema de Audio**: Gestiona música de fondo específica por escena
- **Sistema 3D**: Implementa efectos parallax y transformaciones 3D
- **Gestión de Fotos**: Maneja marcos de fotos arrastrables e interactivos

## Patrones y Convenciones

1. **Gestión de Estado**:
   - `currentSceneIndex` controla la escena activa
   - `is3DMode` gestiona el modo 3D
   - `isMusicPlaying` controla el estado del audio

2. **Estructura CSS**:
   - Variables CSS personalizadas para colores (`--lila-pastel`, `--celeste-bebe`, etc.)
   - Clases específicas por componente (`.scene`, `.photo-frame`, etc.)
   - Animaciones definidas con `@keyframes`

3. **Manejo de Eventos**:
   - Eventos táctiles y de ratón para arrastre
   - Sistema de transiciones con `scene-transition`

## Flujos de Trabajo Críticos

### Agregar Nueva Escena:
1. Añadir configuración en `scenes` array
2. Crear función `loadXXXScene`
3. Actualizar selectores de escena
4. Agregar assets multimedia necesarios

### Implementar Nueva Interacción:
1. Agregar clases CSS necesarias
2. Implementar manejadores de eventos
3. Conectar con sistemas existentes (3D, partículas)

## Tips de Desarrollo

- Prueba en móvil y escritorio - el sitio es responsive
- Verifica la carga de recursos multimedia
- Mantén la consistencia en efectos visuales y transiciones
- Sigue el patrón existente para nuevas características 3D

## Archivos Clave

- `index.html`: Contiene toda la aplicación (HTML, CSS, JS)
- `*.mp3`: Archivos de audio por escena
- `*.jpg, *.png`: Imágenes para la galería

## Integración

Los recursos multimedia se cargan desde rutas GitHub:
```javascript
music: 'https://literland.github.io/mytaekook/Snow%20Flower%20(feat.%20Peakboy).mp3'
```

Al agregar nuevos recursos, asegúrate de mantener la estructura de URLs consistente.