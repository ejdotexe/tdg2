# Tie-Dye Generator: Digital Tie-Dye Simulator

## Project Overview

The Tie-Dye Generator is an innovative web application designed to simulate the art of tie-dyeing digitally. It allows users to experiment with various folding techniques and dye applications on a virtual T-shirt, providing a realistic preview of the final tie-dye pattern. This tool aims to reduce the learning curve and material waste associated with traditional tie-dyeing by offering a safe, digital sandbox for creative exploration.

### Key Features

*   **Web-Based Platform**: Accessible via any modern web browser, with potential for future mobile adaptation.
*   **Hybrid 2D/3D Approach**: Interactive 2D canvas for folding and dyeing, with planned 3D rendering for final visualization.
*   **Realistic Folding Simulation**: Supports multiple folding techniques including spiral, accordion, fan, and fold-in-half, with the ability to layer techniques for complex patterns (e.g., "the spider").
*   **Accurate Dye Application**: Users can apply dye colors with brush controls for size, saturation, and bleed amount.
*   **Subtractive Color Mixing**: Utilizes real Procion MX dye colors (Lemon Yellow, Fuchsia Red, Turquoise, Raven Black) and simulates subtractive color mixing for authentic color blending and bleeding effects.
*   **Intuitive User Interface**: Designed for ease of use, allowing both beginners and experienced tie-dyers to create designs effortlessly.
*   **Downloadable Designs**: Export finished tie-dye patterns as image files.

## Technical Architecture

The application is built using a modern web development stack, focusing on performance, interactivity, and maintainability.

### Frontend

*   **React**: A JavaScript library for building user interfaces, providing a component-based structure for the application.
*   **HTML5 Canvas**: Used for the interactive 2D representation of the T-shirt, handling all folding and dye application logic efficiently.
*   **Three.js (Planned)**: A JavaScript 3D library intended for rendering the final tie-dye design in a rotatable 3D model, offering a more immersive viewing experience.
*   **Tailwind CSS**: A utility-first CSS framework for rapid and responsive UI development.
*   **shadcn/ui**: A collection of re-usable components built with Radix UI and Tailwind CSS, enhancing the application's aesthetic and usability.
*   **Lucide Icons**: A library of open-source icons for clear and concise visual communication.

### Core Logic

1.  **`colorMixing.js`**: Implements subtractive color mixing principles to accurately simulate how real Procion MX dyes blend. It includes utilities for converting between RGB and CMY color spaces, mixing multiple colors, and adjusting saturation.
2.  **`foldingEngine.js`**: Manages the various tie-dye folding techniques. Instead of complex physics, it uses a "layer mapping" approach where each fold defines how pixels are stacked. This allows for efficient calculation of dye penetration through layers.
3.  **`dyeSimulation.js`**: Handles the application of dye to the virtual fabric. It simulates bleeding and diffusion effects, and uses the `foldingEngine` to determine which underlying layers are affected by dye application.

## Setup and Installation

To run the Tie-Dye Generator locally, follow these steps:

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/tie-dye-generator.git
    cd tie-dye-generator
    ```
    *(Note: Replace `your-username` with the actual repository owner's username if this project is hosted on GitHub.)*

2.  **Install dependencies**:
    The project uses `pnpm` for package management. If you don't have `pnpm` installed, you can install it via npm:
    ```bash
    npm install -g pnpm
    ```
    Then, install the project dependencies:
    ```bash
    pnpm install
    ```

3.  **Start the development server**:
    ```bash
    pnpm run dev --host
    ```
    The application will be accessible in your web browser, typically at `http://localhost:5173/`.

## Usage

1.  **Select a Folding Technique**: Use the "Folding Techniques" panel to choose from various folds like Spiral, Accordion, Fan, or Fold in Half. You can layer multiple folds (e.g., Fold in Half, then Spiral for a "spider" effect).
2.  **Choose a Dye Color**: Select one of the authentic Procion MX dye colors from the "Dye Colors" palette.
3.  **Apply Dye**: Click and drag your mouse on the main canvas to apply dye. Observe how the dye spreads and mixes according to the selected folds and brush settings.
4.  **Adjust Brush Settings**: Modify the brush size, dye saturation, and bleed amount using the "Brush Settings" panel for different effects.
5.  **Reset or Download**: Use the "Reset" button to clear your design and start over, or click "Download" to save your finished tie-dye pattern as a PNG image.

## Future Enhancements

*   **3D Rendering**: Implement Three.js to render the final design on a rotatable 3D T-shirt model, allowing users to view their creation from all angles.
*   **Custom Pleating Tool**: Develop a tool for users to draw custom pleating lines, offering even greater control over unique folding patterns.
*   **More Folding Techniques**: Expand the library of pre-defined folding patterns.
*   **Undo/Redo Functionality**: Add history tracking for dye applications and folding steps.
*   **Pattern Saving/Loading**: Allow users to save their in-progress designs and load them later.
*   **Additional Dye Colors**: Integrate a wider range of Procion MX dye colors.
*   **Mobile Responsiveness**: Further optimize the UI and interaction for mobile devices.

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, please open an issue or submit a pull request.

## License

This project is open-source and available under the MIT License.

---

**Developed by Manus AI**

*Using real Procion MX dye colors from Dharma Trading Company for authentic simulation.*
