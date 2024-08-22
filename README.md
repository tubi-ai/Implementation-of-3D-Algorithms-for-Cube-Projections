This report provides an overview of a web-based implementation that demonstrates different 3D rendering techniques using HTML5 and JavaScript. The system is designed to project a 3D cube using various algorithms, each with a specific focus on handling visibility and depth in 3D graphics. The project consists of three primary HTML files (zBuffer.html, cube_hw4.html, and CubeWithBackfaceCulling.html), each illustrating a different algorithm:

1. Z-Buffer Algorithm (zBuffer.html)
Purpose: The Z-Buffer algorithm is a widely used technique in computer graphics for managing image depth coordinates in 3D graphics. It helps in determining which objects, or parts of objects, are visible and which are hidden behind other objects.
Implementation:
The Z-Buffer is represented as an array where each entry corresponds to a pixel on the screen. The array stores depth information for each pixel.
Three colored boxes (red, green, and blue) are defined in 3D space, each with a specific depth (Z value).
The Z-Buffer ensures that for each pixel on the screen, only the closest box (with the lowest Z value) is rendered.
A checkbox allows the user to toggle whether to vary the Z-value per pixel, introducing a sinusoidal variation to the depth, making the rendering more dynamic.
HTML canvas is used for rendering, and sliders control the Z-depth of each box, allowing real-time updates.

2. Custom Cube Rendering (cube_hw4.html)
Purpose: This example showcases a cube with one corner cut off, demonstrating the fundamentals of cube rendering and transformations.
Implementation:
The cube is defined by vertices in 3D space, with connections (edges) drawn between them.
The cube is animated by rotating it around its X, Y, and Z axes, creating a dynamic visualization.
The HTML canvas is used for drawing the cube, with the rotation speed of the cube set via constants.
The code manages vertex transformations and projects the 3D coordinates onto a 2D screen.

3. Backface Culling Algorithm (CubeWithBackfaceCulling.html)
Purpose: The Backface Culling algorithm is used to improve rendering efficiency by not drawing faces of the cube that are not visible to the camera (i.e., the faces that are facing away).

Implementation:
The cube's vertices and faces are defined similarly to the other implementations.
The algorithm calculates the normal vector for each face and determines whether a face is visible or not based on the dot product of the normal and the vector pointing towards the camera.
Non-visible faces (those facing away from the camera) are not rendered, reducing the number of drawn polygons and improving performance.
User Interaction and UI Components
Navbar: Each HTML page includes a responsive navbar allowing users to navigate between different algorithms and see their effects in real-time.
Controls: Sliders and checkboxes are provided to manipulate various parameters (e.g., depth of the boxes in the Z-Buffer example) to observe their effects dynamically.

Conclusion
These implementations demonstrate fundamental 3D graphics algorithms, essential for rendering 3D scenes in real-time applications. The Z-Buffer ensures correct depth rendering, while Backface Culling optimizes performance by reducing the number of polygons to render. This project provides an educational tool for understanding these concepts in a visual and interactive way.
