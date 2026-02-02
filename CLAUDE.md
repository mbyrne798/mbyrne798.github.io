# CLAUDE.md - AI Assistant Guide

This document provides context and guidelines for AI assistants working with this repository.

## Project Overview

This is a **GitHub Pages personal portfolio website** for Mike Robert Byrne. It's a beginner-focused web development project demonstrating core HTML, CSS, and JavaScript skills.

- **Live Site**: [mikerobertbyrne.com](https://mikerobertbyrne.com)
- **Hosting**: GitHub Pages
- **Purpose**: Learning/portfolio project showcasing web fundamentals

## Repository Structure

```
mbyrne798.github.io/
├── CNAME           # GitHub Pages custom domain config (mikerobertbyrne.com)
├── index.html      # Landing page with welcome message
├── game.html       # Interactive "Reach the Goal" browser game
├── style.css       # External stylesheet for index.html
└── CLAUDE.md       # This file
```

## Technology Stack

| Technology | Usage |
|------------|-------|
| HTML5 | Page structure and markup |
| CSS3 | Styling (inline and external) |
| Vanilla JavaScript | Game logic and DOM manipulation |
| GitHub Pages | Static site hosting |

**No build tools, frameworks, or package managers are used.** This is a pure HTML/CSS/JS project.

## File Details

### index.html
- Landing page with welcome message
- Links to external `style.css`
- Contains inline styles for the game button
- Navigation link to `game.html`

### game.html
- Self-contained game page (all CSS/JS inline)
- **Game Features**:
  - 600x400px game container
  - Blue rectangular player (30x50px) controlled by arrow keys
  - Green circular goal (40x40px) with random positioning
  - AABB collision detection
  - Win message modal with "Play Again" functionality
- **Game Constants**:
  - Player speed: 5px per keystroke
  - Container: 600x400px

### style.css
- Global styles for index.html only
- Font: Arial, sans-serif
- Background: #f4f4f4 (light gray)
- Primary button color: #4CAF50 (green)

### CNAME
- Contains: `mikerobertbyrne.com`
- Configures custom domain for GitHub Pages

## Code Conventions

### Naming
- **JavaScript**: camelCase for variables and functions
- **CSS Classes**: kebab-case (e.g., `game-button`, `game-container`)
- **IDs**: kebab-case (e.g., `win-message`, `play-again`)

### Styling Patterns
- Most styles are inline within `<style>` tags in HTML files
- `style.css` provides base typography for the landing page
- Color scheme:
  - Primary green: `#4CAF50` (buttons)
  - Background: `#f4f4f4`
  - Text dark: `#333`
  - Text muted: `#666`

### JavaScript Patterns
- DOM selection via `document.getElementById()`
- Event-driven architecture with keyboard listeners
- Game logic organized into discrete functions:
  - `initGame()` - Setup/reset game state
  - `updateGameObjects()` - Render positions
  - `checkCollision()` - AABB collision detection
- Game state managed via `gameActive` boolean flag

## Development Workflow

### Local Development
1. Clone the repository
2. Open HTML files directly in a browser (no build step required)
3. Use browser DevTools for debugging

### Deployment
- Push to `main` branch triggers automatic GitHub Pages deployment
- Site updates within minutes of push
- Custom domain configured via CNAME file

### Testing
- Manual browser testing only
- Test keyboard controls (arrow keys) for game functionality
- Verify responsive viewport on mobile devices

## Guidelines for AI Assistants

### Do
- Keep changes minimal and focused
- Maintain the vanilla HTML/CSS/JS approach (no frameworks)
- Preserve existing code style and conventions
- Test changes work in modern browsers
- Keep accessibility in mind (keyboard navigation already supported)

### Don't
- Add build tools or package managers unless explicitly requested
- Convert to frameworks (React, Vue, etc.) without user request
- Add unnecessary complexity to this learning project
- Change the custom domain configuration without explicit permission

### When Adding Features
- For new pages: Follow the pattern of existing HTML files
- For new games/interactive elements: Use inline styles/scripts like `game.html`
- For shared styles: Consider if they belong in `style.css` or inline

## Common Tasks

### Adding a New Page
1. Create new `.html` file in root directory
2. Include standard HTML5 boilerplate with viewport meta tag
3. Link to `style.css` or include inline styles
4. Add navigation link from `index.html`

### Modifying the Game
- Player position: `playerX`, `playerY` variables
- Speed: `playerSpeed` constant (currently 5)
- Container size: CSS in `#game-container` (600x400px)
- Goal size: `goalSize` constant (currently 40)

### Updating Styles
- Global typography: Edit `style.css`
- Page-specific styles: Edit inline `<style>` block in respective HTML file
- Button colors: Primary green is `#4CAF50`, hover is `#45a049`
