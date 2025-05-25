# Webpack Basic Setup

A lightweight, modern Webpack 5 starter setup for vanilla JavaScript front-end development. Includes Babel for ES6+ support, CSS handling, and development server with live reload.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Available Scripts](#available-scripts)
- [Project Structure](#project-structure)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)

## Features

- **ES6+ Support**: Write modern JavaScript using Babel and `@babel/preset-env`.
- **Webpack**: Handles JS/CSS bundling and optimizations.
- **HTML Template**: Powered by `html-webpack-plugin` with dynamic title insertion.
- **CSS Support**: Basic setup for importing CSS into JS files.
- **Development Server**: Fast rebuilds with `webpack-dev-server`.

## Getting Started

### Prerequisites

Ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or later)
- npm (comes with Node.js)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/tiagocostarebelo/tcr-webpack-basic-setup.git
   cd tcr-webpack-basic-setup
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

### Available Scripts

- **Start development server**

   ```bash
   npm run dev
   ```

   Launches the app in development mode at [http://localhost:3000](http://localhost:3000). Live reload enabled. Choose your own PORT if you want, by editing the webpack.config.js file.

- **Build for production**

   ```bash
   npm run build
   ```

   Compiles and bundles assets into the `dist/` folder.

## Project Structure

```
tcr-webpack-basic-setup/
├── dist/                     # Bundled output (generated)
├── node_modules/             # Installed dependencies
├── src/                      # Source files
│   ├── styles/
│   │   └── style.css         # Optional custom CSS
│   ├── index.js              # JS entry point (imports CSS)
│   └── template.html         # HTML Webpack template with EJS syntax
├── .gitignore
├── package.json
├── webpack.config.js
└── README.md
```

## Webpack Setup Highlights

- **HTML Webpack Plugin**: Injects JS into `template.html` with dynamic `<%= htmlWebpackPlugin.options.title %>` usage. 
- **Mini CSS Extract Plugin**: For extracting CSS into separate files (optional with `style-loader` fallback).
- **Babel Loader**: Transpiles JS with modern syntax using `@babel/preset-env`.


## Customization

- Add JS modules to `src/` and import as needed.
- Extend `template.html` with additional structure or meta tags. Any edits to `template.html` will reflect in the output only after rebuilding (npm run dev or npm run build).
- Include more loaders/plugins as needed for assets, TypeScript, frameworks, etc.

## Contributing

Pull requests are welcome. Feel free to fork and submit improvements or bug fixes.

## License

This project is licensed under the [MIT License](LICENSE).

---

Created by [Tiago Costa Rebelo](https://github.com/tiagocostarebelo)
