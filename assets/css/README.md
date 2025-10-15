# CSS Architecture

This project uses a modular CSS structure for better organization and maintainability.

## File Structure

```
assets/css/
├── variables.css   - Color variables and CSS custom properties
├── typography.css  - Font styles, headings, links, text
├── layout.css      - Page layout, wrapper, sections, grid
├── sidebar.css     - Sidebar navigation component
├── buttons.css     - Button styles and variations
├── forms.css       - Form inputs, labels, validation
├── main.css        - Core styles and additional components
└── noscript.css    - Fallback styles when JS is disabled
```

## How to Use

### 1. **Changing Colors**

Edit `variables.css` to update all colors across the site:

```css
:root {
  --color-primary: #2b4a7c; /* Change this */
  --bg-sidebar: #2b4a7c; /* Or this */
}
```

### 2. **Modifying Components**

Each component has its own file:

- Sidebar styles → `sidebar.css`
- Buttons → `buttons.css`
- Forms → `forms.css`

### 3. **Layout Changes**

Edit `layout.css` for:

- Wrapper widths
- Section padding
- Grid layouts

### 4. **Typography**

Edit `typography.css` for:

- Font families
- Heading sizes
- Link styles

## Import Order

The CSS files are imported in this order (important for cascade):

1. variables.css (defines colors)
2. typography.css (base text styles)
3. layout.css (page structure)
4. sidebar.css (component)
5. buttons.css (component)
6. forms.css (component)
7. main.css (everything else)

## Benefits

- **Easy Color Changes**: Update all colors from one file
- **Component Isolation**: Edit one component without affecting others
- **Better Performance**: Only load styles you need
- **Easier Debugging**: Find styles faster by file name
- **Team Collaboration**: Multiple people can work on different files
