# Angular Three.js Application

A basic Angular application that integrates Three.js to render a 3D scene with a rotating cube.

## Features

- Angular framework
- Three.js for 3D rendering
- `npm i --save-dev @types/three` for TypeScript support
- Basic lighting setup with directional and ambient lights
- Rotating cube using `MeshPhongMaterial` for enhanced visual clarity

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Node.js (>= 22.x)
- npm (>= 10.x)
- Angular CLI (>= 18.x)

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/manthanank/angular-threejs-app.git
   cd angular-threejs-app
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

## Running the Application

To start the Angular development server and view the application:

```bash
ng serve
```

Navigate to `http://localhost:4200` in your browser to see the application in action. You should see a rotating 3D cube illuminated by both ambient and directional lights.

## Project Structure

- `src/app/three-scene/`
  - `three-scene.component.ts`: Contains the logic for setting up the Three.js scene, lights, and cube.
  - `three-scene.component.html`: Template for the component, which includes a canvas element.
  - `three-scene.component.css`: Basic styling for the canvas element.
  
- `src/app/app.component.html`: Includes the `ThreeSceneComponent` to render it within the main application view.

## Customization

- **Change Cube Color**: Edit the `MeshPhongMaterial` color in `three-scene.component.ts` to change the color of the cube.
  
  ```typescript
  const material = new THREE.MeshPhongMaterial({ color: 0x00ff00 });
  ```

- **Modify Lighting**: Adjust the intensity or position of the lights in the `createLights` method.

  ```typescript
  const directionalLight = new THREE.DirectionalLight(0xffffff, 1);
  directionalLight.position.set(5, 5, 5).normalize();
  ```

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request with your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries or issues, please contact [Manthan Ankolekar](mailto:manthan.ank46@gmail.com).
