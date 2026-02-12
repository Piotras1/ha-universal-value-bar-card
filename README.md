# Universal Value Bar Card (SVG)

A versatile and highly customizable Home Assistant dashboard card built with `custom:button-card` and SVG. This card allows you to display multiple sensors with beautiful, segmented gradients and a clean, modern aesthetic.

## Features
- **SVG Rendering:** Crisp and clear on any device.
- **Segmented Gradients:** Visual representation of values using custom color palettes.
- **Multi-Entity Support: Display as many sensors as you need (Power, Temperature, Battery, etc.) in a single, organized card. No limit on the number of devices.
- **Two Layout Options:** Choose between a standard horizontal view or a more compact layout.
- **Highly Configurable:** Adjust bar length, height, font styles, and spacing.

## Requirements
This card requires the following custom frontend plugin (installable via HACS):
- [button-card](https://github.com/custom-cards/button-card)

## Preview
![Standard Layout](layout1.jpg)
![Compact Layout](layout2.jpg)

## Installation
1. Ensure you have `button-card` installed.
2. Create a new **Manual Card** in your Home Assistant dashboard.
3. Copy the code from [ha-universal-value-bar-card.yaml](ha-universal-value-bar-card.yaml).
4. Customize the `variables` section to match your sensors.

## Configuration (Variables)

| Variable | Description | Default |
| :--- | :--- | :--- |
| `bar_length` | Total width of the bars in pixels | `230` |
| `bar_height` | Thickness of the bars | `12` |
| `spacing` | Vertical distance between items | `44` |
| `card_layout` | Layout style (1: Standard, 2: Compact) | `1` |
| `header` | Title text at the top of the card | `test` |
| `font_size` | Global font size for labels | `13` |
| `c1` - `c10` | Custom color palette (HEX codes) | `Various` |

### Device Settings
Each entry in the `devices` list supports:
- `entity`: The Home Assistant entity ID.
- `name`: Custom display name.
- `min` / `max`: Scale range for the bar.
- `unit`: Measurement unit (e.g., W, °C, %).
- `colors`: A comma-separated list of 5 color indices from the palette (e.g., `1,2,3,4,5`).
- You can add any number of items to the devices list; the card will automatically adjust its height.

## Author
Piotr HA
## License
This project is licensed under the MIT License.
