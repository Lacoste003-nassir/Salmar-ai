# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

Salmar AI is a Flask-based web application that provides an AI interface with a modern, cosmic-themed user interface. The application features glassmorphism design elements, 3D animations using Three.js, and GSAP for smooth transitions.

## Development Commands

### Environment Setup
```bash
# Create and activate virtual environment
python3 -m venv venv
source venv/bin/activate  # On macOS/Linux
# venv\Scripts\activate   # On Windows

# Install dependencies
pip install -r requirements.txt
```

### Running the Application
```bash
# Activate virtual environment first
source venv/bin/activate

# Run Flask development server (when main.py is properly implemented)
python main.py
# Or using Flask CLI
flask run
```

### Development Tasks
```bash
# Check Python syntax
python -m py_compile main.py

# Install new dependencies (remember to update requirements.txt)
pip install package_name
pip freeze > requirements.txt

# View current dependencies
pip list
```

## Architecture Overview

### Project Structure
- `main.py` - Flask application entry point (currently minimal - needs route implementation)
- `templates/` - Jinja2 HTML templates with rich UI components
- `requirements.txt` - Python dependencies
- `venv/` - Virtual environment (not tracked in git)

### Key Templates and Pages
- `home.html` - Landing page with animated cosmic theme
- `AI.html` - Main AI interface with advanced interactive features
- `login.html` / `signup.html` - Authentication pages with glassmorphic design
- `About.html` - About page
- `helpcenter.html` - Help/support center
- Additional utility pages: security, privacy, terms, etc.

### Frontend Technologies
- **Tailwind CSS** - Utility-first CSS framework (loaded via CDN)
- **GSAP** - Animation library for smooth transitions
- **Three.js** - 3D graphics and effects (cosmic orbs, particle systems)
- **Tippy.js** - Tooltips and popovers
- **Lucide Icons** - Icon library

### Design System
- **Theme**: Cosmic/space aesthetic with glassmorphism
- **Colors**: Purple/violet gradient palette with neon accents
- **UI Patterns**: Glass cards, animated orbs, particle effects, neumorphic elements
- **Responsive**: Built with mobile-first approach using Tailwind

### Python Dependencies
Key packages used:
- `Flask` - Web framework
- `requests` - HTTP client
- `beautifulsoup4` - HTML parsing
- `pandas` + `numpy` - Data processing
- `wikipedia` - Wikipedia API access

## Development Notes

### Current State
- `main.py` contains only Flask imports - routes and application logic need to be implemented
- Rich frontend templates are ready but need to be connected to Flask routes
- Virtual environment is set up with Python 3.9

### Frontend Features
- Multiple theme support (dark/light modes in some templates)
- Advanced animations and 3D effects
- Responsive glassmorphic design
- Interactive AI interface components

### Implementation Priorities
1. Implement Flask routes in `main.py` to serve the existing templates
2. Add backend logic for AI interactions
3. Implement authentication system for login/signup pages
4. Connect data processing capabilities (pandas/numpy) for AI features
5. Add proper error handling and logging

### Development Best Practices
- Always work within the virtual environment
- Templates use modern ES6+ JavaScript - ensure browser compatibility
- Heavy use of CDN resources - consider bundling for production
- CSS custom properties used extensively - IE11+ support only