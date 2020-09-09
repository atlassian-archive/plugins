# Mapbox COVID Growth Example

![Mapbox COVID Growth Example](example.png)

Use Mapbox to create a COVID heatmap that changes over time. It expects to have a data per location per day to show growth rate over time.

The data takes the shape of the following JSON:

```json
{
    "dimensions": {
        "width": 830,
        "height": 520
    },
    "metadata": {
        "columns": [
            {
                "label": "date",
                "type": "date",
                "nullable": false
            },
            {
                "label": "latitude",
                "type": "number",
                "nullable": true
            },
            {
                "label": "longitude",
                "type": "number",
                "nullable": true
            },
            {
                "label": "total sum of confirmed",
                "type": "number",
                "nullable": false
            }
        ]
    },
    "data": [
        {
            "date": [
                2020,
                8,
                8
            ],
            "latitude": 38.164046,
            "longitude": -79.124616,
            "total sum of confirmed": 275
        },
       ...
    ],
    "options": {
        "theme": {
            "dashboard": {
                "background": "#eeeeee",
                "grid_color": "#F2F2F2",
                "link_color": "#0b84a5",
                "text_color": "#333333",
                "text_styles": {
                    "h1": {
                        "font_size": 40,
                        "font_weight": "regular"
                    },
                    "h2": {
                        "font_size": 30,
                        "font_weight": "bold"
                    },
                    "h3": {
                        "font_size": 25,
                        "font_weight": "bold"
                    },
                    "comment": {
                        "font_size": 20,
                        "font_weight": "italic"
                    },
                    "paragraph": {
                        "font_size": 20,
                        "font_weight": "regular"
                    }
                }
            },
            "chart": {
                "background": "#ffffff",
                "colors": [
                    "#0b84a5",
                    "#f6c85f",
                    "#6f4e7c",
                    "#9dd866",
                    "#ca472f",
                    "#ffa056",
                    "#8dddd0"
                ],
                "control_background": "#dddddd",
                "zebra_colors_stripe": "#f9f9f9"
            }
        }
    }
}
```