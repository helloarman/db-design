# Database Design Workboard

An interactive, visual database schema designer with a beautiful drag-and-drop interface. Design your database schema visually and generate SQL or Laravel migrations instantly.

🔗 **Live Demo:** [https://helloarman.github.io/db-design](https://helloarman.github.io/db-design)

![Database Design Workboard](https://img.shields.io/badge/status-active-success.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## ✨ Features

### 🎨 Visual Design
- **Drag & Drop Interface** - Smoothly drag tables around the canvas with optimized performance
- **Smart Connections** - Create relationships between tables with visual connection lines
- **Auto Layout** - Automatically arrange tables in a hierarchical flow with proper spacing
- **Zoom & Pan** - Navigate large schemas with mouse wheel zoom and canvas panning
- **Three View Modes** - Switch between Board, List, and Tree views

### 🔗 Relationship Management
- **Visual Connections** - Draw relationships by clicking the link button and connecting tables
- **Hover Effects** - Connection lines and type indicators highlight on hover
- **Clickable Lines** - Select connections to highlight them in blue
- **Relationship Types** - Toggle between 1:1 and 1:N relationships
- **Tooltips** - Hover over lines to see "table → table" relationship names

### 📊 Table Management
- **Quick Create** - Add new tables with automatic ID field
- **Field Management** - Add, remove, and reorder fields via drag & drop
- **Data Types** - Support for 20+ data types including INT, VARCHAR, UUID, ENUM, JSON, etc.
- **Constraints** - Mark fields as primary key, foreign key, or nullable
- **ENUM Values** - Define enum values with tags
- **Rename Tables** - Double-click table name to rename

### 💻 Code Generation
- **SQL Export** - Generate CREATE TABLE statements with foreign keys
- **Laravel Migrations** - Generate Laravel-compatible Schema builder code
- **One-Click Copy** - Copy generated code to clipboard instantly
- **Real-time Preview** - View generated code in dedicated tabs

### 💾 Data Persistence
- **Auto-Save** - All changes automatically saved to localStorage
- **Export/Import** - Export schema as JSON and import later
- **State Management** - Preserves canvas position, zoom level, and all tables

## 🚀 Getting Started

### Quick Start
1. Open the [live demo](https://helloarman.github.io/db-design)
2. Click the **+** button in the left toolbar to create your first table
3. Click the **link** button on a table to create relationships
4. Use the **Beautify** button to auto-arrange tables
5. Switch to **SQL** or **Laravel** tabs to view generated code

### Local Development
```bash
# Clone the repository
git clone https://github.com/helloarman/db-design.git

# Navigate to the directory
cd db-design

# Open index.html in your browser
# No build step required - pure HTML/CSS/JavaScript!
```

## 📖 Usage Guide

### Creating Tables
1. Click the **+** button in the left toolbar
2. Enter a table name (e.g., "User Orders")
3. Preview shows the formatted name (e.g., "user_orders")
4. Click **Create Table**

### Adding Fields
1. Click **Add Field** button at the bottom of any table
2. Edit field name directly inline
3. Select data type from dropdown
4. Toggle **N** button to make field nullable
5. Click **X** to remove a field

### Creating Relationships
1. Click the **link** button on the source table
2. Move mouse away from the card to see the connection line
3. Click on the target table to complete the connection
4. A foreign key field is automatically created in the target table
5. Click the relationship badge to toggle between 1:1 and 1:N

### Reordering Fields
- Drag any field by the grip icon
- Drop it at the desired position
- Works across different tables too!

### View Modes
- **Board View** - Visual canvas with draggable tables
- **List View** - Tables organized by dependency levels
- **Tree View** - Hierarchical tree showing parent-child relationships

### Code Generation
1. Click on **SQL** or **Laravel** tab in any table
2. Review the generated code
3. Click **Copy** button to copy to clipboard
4. Paste into your project

### Auto Layout
Click the **✨ Beautify** button to automatically arrange tables:
- Root tables (no dependencies) on the left
- Dependent tables arranged in levels
- Smart vertical spacing to prevent overlaps
- Parent-child alignment for better readability

## 🎯 Keyboard Shortcuts

- **Ctrl + Scroll** - Zoom in/out
- **Drag Canvas** - Pan around the workspace
- **Double-click Table Name** - Rename table
- **Enter** - Confirm table name or enum value

## 🛠️ Technical Details

### Performance Optimizations
- **RequestAnimationFrame** - Throttled mouse movements for smooth dragging
- **CSS Transforms** - Hardware-accelerated positioning
- **Lazy Rendering** - Deferred connection drawing after DOM updates
- **Will-change Hints** - Browser optimization for transformations

### Technologies Used
- Pure **HTML5/CSS3/JavaScript** (ES6+)
- **Tailwind CSS** via CDN for styling
- **Lucide Icons** for beautiful UI icons
- **SVG** for connection lines and markers
- **LocalStorage API** for data persistence

### Browser Support
- Chrome/Edge (recommended)
- Firefox
- Safari
- Any modern browser with ES6 support

## 📋 Data Types Supported

- **Numeric**: INT, BIGINT, TINYINT, SMALLINT, DECIMAL, FLOAT, DOUBLE
- **String**: VARCHAR, TEXT, LONGTEXT
- **Special**: UUID, BOOLEAN, ENUM, JSON, BINARY
- **Foreign Keys**: foreignId (auto-detected)
- **Date/Time**: DATE, TIME, DATETIME, TIMESTAMP

## 🎨 Features in Detail

### Smart Connection Lines
- Bezier curves for smooth, professional-looking connections
- Automatic side detection (left/right)
- Color-coded relationship type indicators
- Hover to highlight both line and badge
- Click to select and keep highlighted

### Auto Layout Algorithm
- Topological sorting for dependency levels
- Smart vertical positioning based on parent centers
- Collision detection and spacing
- Maintains relationship visibility

### Field Type Intelligence
- Auto-detects foreign keys by naming convention (ends with `_id`)
- Suggests relationships based on field names
- Automatically creates FK constraints in SQL

## 📦 Export/Import Format

```json
{
  "tables": [
    {
      "id": "unique_id",
      "name": "table_name",
      "x": 100,
      "y": 100,
      "color": "border-blue-500",
      "activeTab": "fields",
      "fields": [...]
    }
  ],
  "relations": [
    {
      "id": "rel_id",
      "fromTableId": "source_table_id",
      "toTableId": "target_table_id",
      "type": "1:n",
      "fkFieldId": "field_id"
    }
  ],
  "view": {
    "x": 0,
    "y": 0,
    "scale": 1
  }
}
```

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

MIT License - feel free to use this project for personal or commercial purposes.

## 🙏 Acknowledgments

- Built with ❤️ for database designers and developers
- Inspired by professional database design tools
- Made accessible with a zero-configuration setup

---

**Made by Arman** | [GitHub](https://github.com/helloarman/db-design)