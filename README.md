# Hello Foundry

A simple Foundry VTT module to get started with module development. This project demonstrates basic module structure, TypeScript setup, and development workflows for Foundry Virtual Tabletop.

## Features

- TypeScript support with full Foundry VTT type definitions
- Modern build system using Vite
- Automated development workflow with hot reloading
- SCSS styling support
- ESLint and Prettier for code quality
- Example code demonstrating Foundry VTT APIs

## Installation

### Prerequisites

- [Node.js](https://nodejs.org/) (version 18 or higher recommended)
- [Yarn](https://yarnpkg.com/) package manager
- [Foundry VTT](https://foundryvtt.com/) (version 12 or higher)

### Setup

1. Clone this repository or download the source code
2. Navigate to the project directory
3. Install dependencies:

```bash
yarn install
```

## Development

### Environment Variables (Optional)

You can optionally set these environment variables to customize the development experience:

- `FOUNDRY_DATA_PATH` - Path to your Foundry VTT data directory
- `FOUNDRY_HOST_NAME` - Hostname for the development server (default: localhost)
- `FOUNDRY_PORT` - Port for Foundry VTT (if different from default)

#### Setting Environment Variables

**Windows (PowerShell):**
```powershell
$env:FOUNDRY_DATA_PATH="C:\Users\YourUsername\AppData\Local\FoundryVTT\Data"
$env:FOUNDRY_HOST_NAME="localhost"
```

**Windows (Command Prompt):**
```cmd
set FOUNDRY_DATA_PATH=C:\Users\YourUsername\AppData\Local\FoundryVTT\Data
set FOUNDRY_HOST_NAME=localhost
```

**macOS/Linux:**
```bash
export FOUNDRY_DATA_PATH="/path/to/foundry/data"
export FOUNDRY_HOST_NAME="localhost"
```

### Available Scripts

After running `yarn install`, you can use these commands:

- `yarn dev` - Start development server with hot reloading
- `yarn build` - Build the module for production
- `yarn lint` - Run ESLint on scripts and StyleLint on styles
- `yarn lint:scripts` - Run ESLint on TypeScript files only
- `yarn lint:styles` - Run StyleLint on CSS/SCSS files only
- `yarn format` - Format code with Prettier
- `yarn typecheck` - Run TypeScript type checking

### Development Workflow

1. Run `yarn dev` to start the development server
2. The module will be automatically built and can be hot-reloaded during development
3. Make your changes to the source files in the `src/` directory
4. The build system will automatically compile TypeScript and SCSS files

## Project Structure

```
├── src/
│   ├── module/          # TypeScript module source files
│   │   └── index.ts     # Main module entry point
│   └── styles/          # SCSS stylesheets
│       └── styles.scss  # Main stylesheet
├── module.json          # Foundry VTT module manifest
├── package.json         # Node.js dependencies and scripts
├── vite.config.ts       # Vite build configuration
├── tsconfig.json        # TypeScript configuration
├── eslint.config.js     # ESLint configuration
└── utils.ts             # Build utilities
```

## Module Configuration

The module is configured through `module.json`:

- **ID**: `hello-foundry`
- **Title**: Hello Foundry
- **Compatibility**: Foundry VTT v12+ (verified up to v13)
- **Entry Point**: `index.js` (compiled from `src/module/index.ts`)
- **Styles**: `styles.css` (compiled from `src/styles/styles.scss`)

## Building for Production

To create a production build:

```bash
yarn build
```

This will generate the compiled module files that can be installed in Foundry VTT.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run `yarn lint` and `yarn typecheck` to ensure code quality
5. Submit a pull request

## License

This project is provided as a starting template for Foundry VTT module development.

## Support

For Foundry VTT development questions, consult:
- [Foundry VTT Documentation](https://foundryvtt.com/kb/)
- [Foundry VTT Community Discord](https://discord.gg/foundryvtt)
- [League of Foundry Developers](https://github.com/League-of-Foundry-Developers)

