// Create the overlay and SVG elements
const overlay = document.createElement('div');
overlay.id = 'loader';
overlay.style.cssText = `
    display: flex;
    justify-content: center;
    align-items: center;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(255, 255, 255, 0.7);
    z-index: 999;
`;

const svgImage = document.createElement('img');
svgImage.id = 'svgImage';
svgImage.src = 'https://github.com/andresacero-brokerfy/preloader/blob/0dd8803f444149b0de11432af4f7ec906b9e070a/loading_providencia.svg';
svgImage.style.cssText = `
    width: 120px;  // Ancho fijo de 120px
    height: auto;  // Alto se ajusta automáticamente
    display: none;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
`;

// Append the elements to the body
document.body.appendChild(overlay);
document.body.appendChild(svgImage);

// Function to hide the overlay and display the SVG
function hideOverlay() {
    overlay.style.display = 'none';
    svgImage.style.display = 'block';
}

// Add an event listener to hide the overlay when all external JS files are loaded
document.addEventListener('DOMContentLoaded', () => {
    setTimeout(hideOverlay, 100);
});

// Fallback: If all external resources are loaded and the DOMContentLoaded event doesn't fire,
// we'll still hide the overlay when the window's load event is triggered.
window.addEventListener('load', hideOverlay);
