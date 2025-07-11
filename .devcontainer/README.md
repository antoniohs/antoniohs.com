# Hugo Development Container

This repository includes a VS Code development container configuration that provides a consistent development environment for Hugo websites.

## What's Included

- **Hugo Extended**: Latest version with SCSS/SASS support
- **Go 1.24**: Latest stable version for Hugo and theme development
- **Useful VS Code Extensions**:
  - TOML support for config files
  - Markdown editing and preview
  - Prettier for code formatting
  - Tailwind CSS support
  - Go language support

## Getting Started

1. **Prerequisites**:
   - Install [VS Code](https://code.visualstudio.com/)
   - Install the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
   - Install [Docker](https://www.docker.com/get-started)

2. **Open in Container**:
   - Open this project in VS Code
   - When prompted, click "Reopen in Container"
   - Or use the Command Palette: `Dev Containers: Reopen in Container`

3. **Development**:
   - Hugo server will be available at `http://localhost:1313`
   - Port 1313 is automatically forwarded
   - Use the built-in tasks for common operations

## Available Tasks

Access these through the Command Palette (`Ctrl+Shift+P`) → "Tasks: Run Task":

- **Hugo: Serve** - Start the development server with drafts and future posts
- **Hugo: Build** - Build the site for production
- **Hugo: Clean** - Remove build artifacts
- **Hugo: New Post** - Create a new post with a custom name

## Direct Hugo Commands

You can run Hugo commands directly in the terminal:

- `hugo server` - Start development server
- `hugo --minify` - Build for production
- `rm -rf public resources` - Clean build artifacts
- `hugo new posts/my-post.md` - Create a new post

## File Structure

The container automatically:
- Updates Hugo modules on creation
- Excludes build artifacts from search/file explorer
- Configures formatters and editor settings

## Customization

To modify the container configuration:
1. Edit `.devcontainer/devcontainer.json`
2. Rebuild the container: `Dev Containers: Rebuild Container`

For additional dependencies, update the `devcontainer.json` features section. 