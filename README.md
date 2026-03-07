# Raytracer - 3D Scene Renderer 🎨✨

A real-time 3D raytracing renderer built with C++ and SDL2. Create and visualize stunning 3D scenes with realistic lighting, shadows, and reflections. Interact with the scene using mouse and keyboard controls.

![Raytracing Preview](./Screenshot.png)

## 🎯 What Does It Do?

This raytracer renders 3D scenes in real-time with:

- **3D Rendering**: Visualize complex 3D scenes with spheres, planes, and other objects
- **Realistic Lighting**: Accurate light simulation with shadows and reflections
- **Interactive Controls**: Rotate, zoom, and navigate through the scene
- **Real-Time Updates**: See changes instantly as you interact
- **Ray-Object Intersection**: Precise mathematical calculations for realistic rendering
- **Color and Materials**: Different materials with varying properties
- **Ambient Occlusion**: Soft shadows for depth perception

## 👤 Who Is It For?

- Computer graphics students learning raytracing
- Game developers understanding rendering techniques
- 3D artists exploring rendering algorithms
- Programmers interested in graphics programming
- Anyone fascinated by computer-generated imagery

## 🚀 How to Use

### Prerequisites

- **C++ Compiler** (g++ or clang)
- **SDL2 Library** - For window management and rendering
- **Make** - Build automation tool

### Installation

#### 1. Install SDL2

**macOS:**
```bash
brew install sdl2
```

**Ubuntu/Debian:**
```bash
sudo apt-get update
sudo apt-get install libsdl2-dev
```

**Fedora:**
```bash
sudo dnf install SDL2-devel
```

**Windows:**
- Download SDL2 development libraries from [SDL2 Downloads](https://www.libsdl.org/download-2.0.php)
- Extract and configure in your project

#### 2. Clone and Build

```bash
# Clone the repository
git clone https://github.com/mohammedhrima/Raytracer.git
cd Raytracer

# Build the project
make

# This creates the executable 'exec'
```

### Running the Raytracer

```bash
./exec
```

A window will open displaying the rendered 3D scene.

## 🎮 Interactive Controls

### Mouse Controls

**Rotate the Scene:**
- **Left-click and drag**: Rotate the camera around the scene
- Move mouse left/right: Rotate horizontally
- Move mouse up/down: Rotate vertically

**Zoom:**
- **Scroll wheel up**: Zoom in (get closer to objects)
- **Scroll wheel down**: Zoom out (move away from objects)

### Keyboard Controls

**Navigate the Scene:**
- **↑ (Up Arrow)**: Move camera upward
- **↓ (Down Arrow)**: Move camera downward
- **← (Left Arrow)**: Move camera left
- **→ (Right Arrow)**: Move camera right

**Exit:**
- **ESC**: Close the application

## ✨ Features

### Raytracing Techniques

**Ray Generation:**
- Generates rays from camera through each pixel
- Calculates ray direction based on camera position and orientation

**Intersection Testing:**
- Ray-sphere intersection
- Ray-plane intersection
- Efficient intersection algorithms

**Lighting Model:**
- Diffuse lighting (Lambertian reflection)
- Specular highlights
- Ambient lighting
- Shadow rays for realistic shadows

**Color Calculation:**
- RGB color mixing
- Material properties (color, reflectivity)
- Light intensity calculations

### Scene Elements

The default scene includes:
- Multiple spheres of different sizes and colors
- Ground plane
- Light sources
- Camera with adjustable position

### Performance

- Real-time rendering at interactive frame rates
- Optimized intersection calculations
- Efficient memory management

## 🛠️ Technical Stack

- **C++98**: Core programming language
- **SDL2**: Simple DirectMedia Layer for graphics
- **Mathematics**: Vector math, ray equations, intersection algorithms
- **Make**: Build system

## 📁 Project Structure

```
Raytracer/
├── Makefile              # Build configuration
├── README.md             # This file
├── Screenshot.png        # Preview image
├── header.hpp            # Header files and declarations
├── main.cpp              # Entry point and main loop
├── math.cpp              # Vector and matrix mathematics
├── raytracing.cpp        # Core raytracing algorithms
├── window.cpp            # SDL window management
├── new.cpp               # Memory management
└── SDL/                  # SDL2 header files
    ├── SDL.h
    ├── SDL_events.h
    ├── SDL_video.h
    └── ... (other SDL headers)
```

## 🔧 Building and Compilation

### Build Commands

```bash
# Compile the project
make

# Clean build files
make clean

# Rebuild everything
make re
```

### Compilation Details

The Makefile compiles these source files:
- `main.cpp` - Application entry point
- `math.cpp` - Mathematical operations
- `raytracing.cpp` - Raytracing algorithms
- `window.cpp` - Window and event handling
- `new.cpp` - Memory management

Flags used:
- `-std=c++98` - C++98 standard
- `-Wall -Wextra -Werror` - Strict warnings
- `-lSDL2` - Link SDL2 library

## 🎨 Understanding Raytracing

### How Raytracing Works

1. **Camera Setup**: Define camera position and viewing direction
2. **Ray Generation**: For each pixel, create a ray from camera through pixel
3. **Intersection Testing**: Check if ray hits any objects in scene
4. **Shading**: Calculate color based on:
   - Object material
   - Light sources
   - Shadows
   - Reflections
5. **Pixel Coloring**: Set pixel to calculated color

### Ray Equation

```
Ray(t) = Origin + t * Direction
```

Where:
- `Origin` = Camera position
- `Direction` = Ray direction through pixel
- `t` = Distance along ray

### Sphere Intersection

Solving the equation:
```
|Ray(t) - SphereCenter|² = SphereRadius²
```

Results in a quadratic equation that determines if and where the ray hits the sphere.

## 🎓 Learning Outcomes

This project demonstrates:
- **Ray-object intersection algorithms**
- **3D vector mathematics**
- **Lighting models and shading**
- **Real-time graphics programming**
- **SDL2 for window management**
- **Event handling (mouse, keyboard)**
- **Performance optimization**

## 🔧 Customization

### Modify the Scene

Edit `raytracing.cpp` to:
- Add more spheres
- Change sphere positions and sizes
- Modify colors and materials
- Add different light sources
- Change background color

### Adjust Camera

Edit `main.cpp` to:
- Change initial camera position
- Modify field of view
- Adjust movement speed
- Change rotation sensitivity

### Enhance Rendering

Possible improvements:
- Add more object types (cubes, cylinders)
- Implement reflections and refractions
- Add texture mapping
- Implement anti-aliasing
- Add depth of field effects

## 📊 Performance Tips

**Optimize Rendering:**
- Reduce window resolution for faster rendering
- Limit number of objects in scene
- Use bounding volumes for complex objects
- Implement spatial data structures (BVH, octree)

**Improve Quality:**
- Increase ray samples per pixel
- Add more light bounces
- Implement global illumination
- Use higher precision calculations

## 🐛 Troubleshooting

**SDL2 not found:**
```bash
# Verify SDL2 installation
sdl2-config --version

# If not found, reinstall SDL2
```

**Compilation errors:**
```bash
# Clean and rebuild
make clean
make
```

**Window doesn't open:**
- Check if SDL2 is properly installed
- Verify display is available
- Check for error messages in terminal

**Slow performance:**
- Reduce window size
- Simplify scene (fewer objects)
- Close other applications

## 📈 Future Enhancements

- [ ] Add more primitive shapes (cubes, cylinders, cones)
- [ ] Implement reflection and refraction
- [ ] Add texture mapping
- [ ] Implement anti-aliasing (supersampling)
- [ ] Add global illumination
- [ ] Support for loading 3D models (OBJ files)
- [ ] Path tracing for photorealistic rendering
- [ ] GPU acceleration with CUDA or OpenCL
- [ ] Scene file format for easy scene creation
- [ ] Real-time scene editing

## 🤝 Contributing

Contributions welcome! Great project for learning:
- Computer graphics
- Raytracing algorithms
- C++ programming
- SDL2 library

## 📚 Resources

**Learn More About Raytracing:**
- [Ray Tracing in One Weekend](https://raytracing.github.io/)
- [Scratchapixel - Ray Tracing](https://www.scratchapixel.com/lessons/3d-basic-rendering/introduction-to-ray-tracing)
- [SDL2 Documentation](https://wiki.libsdl.org/)

**Mathematics:**
- Vector operations
- Ray-sphere intersection
- Lighting equations (Phong, Blinn-Phong)

## 📄 License

This project is open source and available for educational purposes.

## 🙏 Acknowledgments

- SDL2 team for the excellent graphics library
- Computer graphics community for raytracing resources
- Classic raytracing papers and books
