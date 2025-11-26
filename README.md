# Musical Tonnetz Visualizer

An interactive 3D visualization tool for exploring musical scales, chords, and harmonic relationships in a cylindrical pitch space.

## Overview

This web application creates a three-dimensional "tonnetz" (tone network) that displays all 128 MIDI notes arranged in a helical structure. Notes are organized in layers of 12 (corresponding to the chromatic scale), with each layer stacked vertically to represent octaves.

## Features

- **3D Interactive Visualization**: Rotate, pan, and zoom to explore the pitch space from any angle
- **Scale Highlighting**: Visualize musical scales with color-coded notes
- **Chord Display**: Show chord notes with connecting lines to illustrate harmonic relationships
- **Degree Marking**: Highlight specific scale degrees in red
- **Animation Mode**: Automatically cycle through multiple scales and chord progressions
- **Mobile Responsive**: Touch controls optimized for mobile devices

## Controls

### Navigation
- **Mouse**: Click and drag to rotate the camera
- **Mouse Wheel**: Scroll to zoom in/out
- **Touch**: Single finger drag to rotate, two-finger pinch to zoom
- **Reset Camera**: Return to the default viewing angle

### Input Fields

1. **Scales**: Enter scale patterns as comma-separated pitch classes
   - Multiple scales separated by semicolons
   - Example: `0,2,4,5,7,9,11; 0,2,3,5,7,8,11`
   - Represents C Major; C Minor

2. **Chords**: Enter MIDI note numbers for chord notes
   - Multiple chords separated by semicolons
   - Example: `60,64,67; 59,62,67`
   - Represents C Major triad; B diminished triad

3. **Degrees**: Enter scale degree indices
   - Separated by semicolons (one per scale)
   - Example: `1; 4; 0`
   - 0 = first degree (tonic), 1 = second degree, etc.

## Color Coding

- **Orange**: Root note of the scale (largest sphere)
- **Cyan**: Other notes in the scale
- **Yellow**: Chord notes with connecting lines
- **Red**: Highlighted scale degree
- **Dark Gray**: Notes not in the current scale

## Default Visualization

The app loads with a demonstration showing:
- C Major scale (0,2,4,5,7,9,11)
- Three chord progression
- Automatic transitions every 1.5 seconds

## Technical Details

- Built with Three.js (r128)
- Renders 128 spheres representing MIDI notes 0-127
- Optimized performance for mobile devices
- No external dependencies beyond Three.js

## Usage Examples

### Major Scale Progression
```
Scales: 0,2,4,5,7,9,11; 0,2,4,5,7,9,11; 0,2,4,5,7,9,11; 0,2,4,5,7,9,11
Chords: 60,64,67; 65,69,72; 67,71,74; 60,64,67
Degrees: 0; 3; 4; 0
```

### Minor ii-V-i Progression
```
Scales: 0,2,3,5,7,8,10; 0,2,3,5,7,8,10; 0,2,3,5,7,8,10
Chords: 62,65,69; 65,68,71,74; 60,63,67
Degrees: 1; 4; 0
```

## Browser Compatibility

Works in all modern browsers with WebGL support:
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

## License

Open source - feel free to modify and use as needed.
