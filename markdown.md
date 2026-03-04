# UI Design Guidelines

## Overview
Clean, minimal, brutalist-lite UI system for plugins and desktop applications.
Functional and raw — structure comes from borders and spacing, not depth or decoration.
Consistent across light and dark modes.

---

## Typography

- **Font:** Inter (all weights)
- **Section labels:** uppercase, letter-spacing: 0.08em, font-size: 11px, color: `--color-text-muted`
- **Body text:** 13–14px, regular weight
- **Button text:** 13px, medium (500), uppercase for primary actions only
- **No decorative or display fonts**

---

## Color System

### Light Mode
| Token | Value | Usage |
|---|---|---|
| `--color-bg` | `#F5F5F5` | App/panel background |
| `--color-surface` | `#FFFFFF` | Cards, inputs, dropdowns |
| `--color-border` | `#D4D4D4` | Strokes on buttons, inputs, dividers |
| `--color-text` | `#171717` | Primary text |
| `--color-text-muted` | `#737373` | Labels, hints, secondary text |
| `--color-header-bg` | `#1E1E1E` | Title bar / header area |
| `--color-header-text` | `#F5F5F5` | Text on dark header |
| `--color-selected-bg` | `#171717` | Active/selected button fill |
| `--color-selected-text` | `#FFFFFF` | Text on selected button |

### Dark Mode (inverse)
| Token | Value | Usage |
|---|---|---|
| `--color-bg` | `#171717` | App/panel background |
| `--color-surface` | `#262626` | Cards, inputs, dropdowns |
| `--color-border` | `#404040` | Strokes on buttons, inputs, dividers |
| `--color-text` | `#F5F5F5` | Primary text |
| `--color-text-muted` | `#737373` | Labels, hints, secondary text |
| `--color-header-bg` | `#0A0A0A` | Title bar / header area |
| `--color-header-text` | `#F5F5F5` | Text on dark header |
| `--color-selected-bg` | `#F5F5F5` | Active/selected button fill |
| `--color-selected-text` | `#171717` | Text on selected button |

### Accent Colors (both modes)
| Token | Value | Usage |
|---|---|---|
| `--color-success` | `#22C55E` | Success states, confirmations |
| `--color-warning` | `#EAB308` | Warnings, caution states |
| `--color-error` | `#EF4444` | Errors, destructive actions |
| `--color-info` | `#3B82F6` | Info, links, highlights |

---

## Spacing

Base unit: **4px**

| Token | Value |
|---|---|
| `--space-1` | 4px |
| `--space-2` | 8px |
| `--space-3` | 12px |
| `--space-4` | 16px |
| `--space-5` | 24px |
| `--space-6` | 32px |
| `--space-7` | 48px |
| `--space-8` | 64px |

---

## Border Radius

| Token | Value | Usage |
|---|---|---|
| `--radius-sm` | 4px | Buttons, inputs, tags |
| `--radius-md` | 6px | Cards, dropdowns, panels |
| `--radius-lg` | 8px | Modals, large surfaces |
| `--radius-full` | 9999px | Toggles, badges, pills |

---

## Borders & Strokes

- All interactive elements (buttons, inputs, dropdowns) have a visible `1px` border using `--color-border`
- No borders on backgrounds or layout containers
- Dividers: `1px solid --color-border`
- No box shadows — use borders and spacing for structure

---

## Components

### Buttons

**Default (outline)**
- Background: `--color-surface`
- Border: `1px solid --color-border`
- Text: `--color-text`, 13px, medium
- Padding: `--space-2` vertical, `--space-3` horizontal
- Border radius: `--radius-sm`

**Selected / Primary (filled)**
- Background: `--color-selected-bg`
- Border: `1px solid --color-selected-bg`
- Text: `--color-selected-text`, uppercase, 13px, medium
- Same padding and radius as default

**Destructive**
- Background: `--color-error` (filled) or transparent (outline)
- Border: `1px solid --color-error`
- Text: white (filled) or `--color-error` (outline)

**Hover states**
- Outline button: background shifts to `--color-border` (subtle fill)
- No transitions longer than 100ms — keep it snappy

**Disabled**
- Opacity: 0.4
- Cursor: not-allowed

---

### Inputs & Text Fields

- Background: `--color-surface`
- Border: `1px solid --color-border`
- Border radius: `--radius-sm`
- Padding: `--space-2` vertical, `--space-3` horizontal
- Font: Inter 13px, `--color-text`
- Placeholder: `--color-text-muted`
- Focus: border becomes `--color-text` (light) or `--color-selected-bg` (dark)
- No glow, no coloured focus ring

---

### Dropdowns / Selects

- Same appearance as inputs
- Chevron icon (Lucide `ChevronDown`), `--color-text-muted`
- Dropdown menu: `--color-surface`, `1px solid --color-border`, `--radius-md`
- Menu items: 13px, full-width, padding `--space-2` vertical `--space-3` horizontal
- Hover: background `--color-bg`
- Selected item: bold or checkmark (Lucide `Check`)

---

### Toggles / Switches

- Track: `--color-border` (off), `--color-success` (on)
- Thumb: white, circular (`--radius-full`)
- Size: 32px × 18px track, 14px thumb
- No labels inside the track
- Label text sits beside toggle, `--color-text`, 13px

---

### Tabs / Segmented Controls

- Container: no background, bottom border `1px solid --color-border`
- Active tab: bottom border `2px solid --color-text`, text `--color-text`, medium weight
- Inactive tab: text `--color-text-muted`, regular weight
- No pill/filled tab style — underline only
- Icons optional, use Lucide, 16px, aligned with label

---

### Section Labels

- Uppercase
- Font size: 11px
- Letter spacing: 0.08em
- Color: `--color-text-muted`
- Margin bottom: `--space-2`
- No bold weight

---

### Dividers

- `1px solid --color-border`
- Full width
- Margin: `--space-4` vertical

---

### Cards / Panels

- Background: `--color-surface`
- Border: `1px solid --color-border`
- Border radius: `--radius-md`
- Padding: `--space-4`
- No shadow

---

### Modals / Dialogs

- Overlay: `rgba(0,0,0,0.5)`
- Modal surface: `--color-surface`, `--radius-lg`, `1px solid --color-border`
- Header: bold title, 15px, close button (Lucide `X`) top right
- Footer: right-aligned actions, divider above
- Max width: 480px for standard dialogs
- No shadow on modal itself — border provides definition

---

### Toasts / Notifications

- Appear bottom-right (desktop) or bottom-center (plugin)
- Background: `--color-selected-bg` (inverted from current mode for contrast)
- Text: `--color-selected-text`
- Border: `1px solid --color-border`
- Border radius: `--radius-md`
- Padding: `--space-3` vertical, `--space-4` horizontal
- Include accent left border for typed toasts:
  - Success: `4px solid --color-success`
  - Warning: `4px solid --color-warning`
  - Error: `4px solid --color-error`
  - Info: `4px solid --color-info`
- Auto-dismiss after 4s, no animation longer than 150ms

---

### Sidebars / Panels

- Background: `--color-bg`
- Border right/left: `1px solid --color-border`
- Width: 240–280px (desktop), full-width (plugin panels)
- Nav items: 13px, `--color-text-muted`, padding `--space-2` vertical `--space-3` horizontal
- Active nav item: `--color-text`, medium weight, background `--color-surface`

---

### Tables

- Header row: uppercase labels, 11px, `--color-text-muted`, letter-spacing 0.08em
- Row border: `1px solid --color-border` bottom only
- Row hover: background `--color-bg`
- Cell padding: `--space-2` vertical, `--space-3` horizontal
- No zebra striping
- No outer border on table itself

---

## Icons

- Library: **Lucide**
- Default size: **16px** (inline), **20px** (standalone/actions)
- Stroke width: **1.5px**
- Color: inherits from text context (`--color-text` or `--color-text-muted`)
- No filled icon variants

---

## Header / Title Bar

- Background: `--color-header-bg`
- Text: `--color-header-text`, 13px, medium
- Height: ~48px
- Icon or logo on left, close/window controls on right
- No bottom border needed — contrast provides separation

---

## General Rules

- **No box shadows anywhere**
- **No gradients**
- **No animations longer than 150ms**
- **Structure comes from borders and spacing, not depth**
- **Consistency over creativity** — when in doubt, use what already exists in these guidelines
- **4px grid strictly** — all spacing, sizing, and positioning must snap to 4px increments
- All interactive elements must have a clear hover and active state
- Disabled states use 0.4 opacity
