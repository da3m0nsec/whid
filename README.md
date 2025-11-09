# WHID - What Have I Done

<div align="center">
  <img src="logo.png" alt="WHID Logo" width="200"/>

  **Track your progress, one check at a time.**

  A beautiful, interactive checklist application for tracking tasks with visual feedback and persistent state management.
</div>

---

## Overview

WHID (What Have I Done) is a modern, browser-based checklist application designed to help you track project progress with style. Whether you're managing a development sprint, completing a QA checklist, or tracking any step-by-step process, WHID provides an intuitive interface with rich features.

## Features

### Core Functionality
- **YAML-Based Checklists** - Load and save checklists using simple YAML files
- **Visual Progress Tracking** - Real-time statistics showing success, failed, and pending items
- **Status Management** - Mark items as success or failed with optional comments
- **Drag & Drop Reordering** - Easily reorganize items by dragging them
- **Dynamic Item Management** - Add or delete items on the fly
- **Persistent Metadata** - Track checklist name, notes, and last modified date

### User Experience
- **Clean, Modern UI** - Beautiful gradient design with smooth animations
- **Responsive Layout** - Works seamlessly on different screen sizes
- **Interactive Feedback** - Visual cues for all actions
- **Comment System** - Add context to success or failure states
- **Progress Visualization** - Color-coded stats and progress bar

### Technical Features
- **Pure JavaScript** - No dependencies except js-yaml for parsing
- **Local File System** - Save and load files directly from your computer
- **File System Access API** - Modern "Save As" dialog support
- **Single Page Application** - Runs entirely in your browser
- **No Backend Required** - Everything runs client-side

## Getting Started

### Installation

1. Clone or download this repository
2. Open `whid.html` in your web browser

That's it! No build process, no dependencies to install.

### Basic Usage

#### Creating a New Checklist

1. Click the "Create New Checklist" button
2. Fill in the checklist name and notes (optional)
3. Add items using the input field at the bottom
4. Track your progress as you work through items

#### Loading an Existing Checklist

1. Click "Choose File" and select a `.yaml` or `.yml` file
2. The checklist will load automatically with any saved progress
3. Continue where you left off

#### Working with Items

- **Mark as Success**: Click the green checkmark button
- **Mark as Failed**: Click the red X button
- **Add Comment**: After marking an item, click "Add Comment" to provide context
- **Reset Status**: Click "Reset" to return an item to pending state
- **Reorder Items**: Drag items using the handle (⋮⋮) on the left
- **Delete Items**: Click the trash icon to remove an item

#### Saving Your Work

- **Download Checklist**: Saves with the current filename
- **Save As**: Opens a save dialog to choose location and filename

## YAML Format

WHID uses a simple YAML structure:

### Basic Format
```yaml
items:
  - Review project requirements
  - Set up development environment
  - Create database schema
  - Implement user authentication
```

### Full Format with Metadata
```yaml
name: Development Sprint Checklist
notes: Sprint 23 - Authentication Feature
lastModified: 2025-11-08
checklist:
  - item: Review project requirements
    status: success
    comment: All requirements documented in Confluence
  - item: Set up development environment
    status: success
  - item: Create database schema
    status: failed
    comment: Missing foreign key constraint on users table
  - item: Implement user authentication
    status: pending
```

### Supported Properties

- **name**: Checklist title (optional)
- **notes**: Additional context or description (optional)
- **lastModified**: Auto-updated on save (YYYY-MM-DD format)
- **items** or **checklist**: Array of checklist items
  - **item**: The task description (required)
  - **status**: `pending`, `success`, or `failed` (default: `pending`)
  - **comment**: Optional note about the item's status

## File Structure

```
whid/
├── whid.html              # Main application file
├── logo.png               # Application logo (80x80)
├── logo-background.png    # Background logo asset
├── logo - whid.png        # Alternative logo design
├── example-checklist.yaml # Sample checklist template
└── README.md             # This file
```

## Browser Compatibility

WHID works best in modern browsers that support:
- HTML5
- CSS3 (Grid, Flexbox, Gradients)
- ES6 JavaScript
- File System Access API (optional, for "Save As" functionality)

Tested and verified on:
- Google Chrome 90+
- Microsoft Edge 90+
- Mozilla Firefox 88+
- Safari 14+

## Tips & Tricks

- **Keyboard Shortcut**: Press Enter in the "Add item" field to quickly add items
- **Click the Logo**: Returns to the home screen (with confirmation if checklist is loaded)
- **Auto-Dating**: Filenames automatically include the current date when saving
- **Visual Cues**: Green for success, red for failed, neutral for pending
- **Comment Later**: You can add or edit comments after marking an item

## Use Cases

- **Software Development**: Sprint checklists, QA testing procedures, deployment steps
- **Project Management**: Milestone tracking, onboarding processes, audit checklists
- **Personal Productivity**: Daily routines, travel packing lists, maintenance schedules
- **Education**: Assignment tracking, study guides, research checklists
- **Operations**: Server deployment, configuration verification, incident response

## Development

### Making Changes

The application is contained in a single HTML file with embedded CSS and JavaScript. To modify:

1. Open [whid.html](whid.html) in your text editor
2. Find the relevant section:
   - Styles: `<style>` tag (lines 8-748)
   - Structure: `<body>` tag (lines 750-853)
   - Logic: `<script>` tag (lines 856-1610)
3. Make your changes
4. Refresh in browser to test

### Customization Ideas

- Modify colors in the CSS gradient (`.header`, `.container`)
- Add new status types beyond success/failed
- Implement local storage for auto-save
- Add export formats (JSON, CSV, Markdown)
- Create keyboard shortcuts for common actions

## License

This project is open source and available for personal and commercial use.

## Contributing

Found a bug or have a feature request? Feel free to:
- Open an issue
- Submit a pull request
- Fork and customize for your needs

## Acknowledgments

- Built with vanilla JavaScript and modern web standards
- Uses [js-yaml](https://github.com/nodeca/js-yaml) for YAML parsing
- Inspired by the need for simple, visual progress tracking

---

<div align="center">
  Made with care for tracking progress step by step.

  **WHID** - What Have I Done
</div>
