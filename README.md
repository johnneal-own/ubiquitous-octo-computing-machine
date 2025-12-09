# 360° Panorama Viewer with Eye Frame

An interactive 360° panorama viewer with a binocular/VR goggle-style eye frame overlay, ready to embed into any website.

## Features

- **360° Panorama View**: Full spherical panorama support using A-Frame
- **Eye Frame Overlay**: Binocular/VR goggle-style frame for immersive viewing experience
- **Interactive Controls**: Click and drag to look around, WASD/arrow keys for navigation
- **VR Mode**: Built-in VR mode support for compatible devices
- **Mobile Friendly**: Gyroscope support for mobile devices
- **Easy Embedding**: Simple iframe integration for any website
- **Accessibility**: Toggle button to show/hide eye frame overlay, with preference saved locally

## Files

- **panorama.html**: The main 360° panorama viewer with eye frame overlay
- **iframe.html**: Example embedding page showing how to integrate the viewer
- **7CCB8559-C96A-4DE3-B847-10F4AB3035AF_L0_001-24_06_2025, 16_37_35.jpg**: The 360° panorama image (8192x4096 equirectangular format)

## Usage

### View Locally

1. Open `panorama.html` directly in a web browser
2. Or open `iframe.html` to see the embed example

### Embed in Your Website

Add this code to your HTML:

```html
<iframe 
  width="1200" 
  height="700" 
  src="panorama.html" 
  style="border: none;"
  allowfullscreen
  allow="accelerometer; gyroscope; vr"
  title="360 Panorama Viewer">
</iframe>
```

For responsive embedding, use this CSS:

```css
.panorama-container {
  position: relative;
  width: 100%;
  padding-bottom: 58.33%; /* 1200:700 aspect ratio */
}

.panorama-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: none;
}
```

Then wrap your iframe:

```html
<div class="panorama-container">
  <iframe src="panorama.html" allowfullscreen></iframe>
</div>
```

## Controls

- **Mouse**: Click and drag to look around
- **Keyboard**: WASD or arrow keys to navigate
- **Mobile**: Move device to look around (gyroscope)
- **VR Mode**: Click VR button in bottom-right corner
- **Toggle Eye Frame**: Click the "👁️ Toggle Eye Frame" button (top-right) to show/hide the overlay for better accessibility

## Customization

### Change the Eye Frame Style

Edit the SVG in `panorama.html` to customize:
- Circle sizes and positions for different eye frame shapes
- Colors and opacity for different frame styles
- Add additional decorative elements

### Replace the Panorama Image

Replace the image file with your own 360° panorama (equirectangular format, 2:1 aspect ratio recommended) and update the `src` attribute in the `<a-sky>` element.

## Technology

- **A-Frame**: WebVR framework for 360° panorama rendering
- **SVG**: Scalable Vector Graphics for the eye frame overlay
- **Pure HTML/CSS/JS**: No build process required
