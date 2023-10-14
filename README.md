QTILE_TABBED
============

Proof-of-concept Tabbed layout in Qtile.

The layout maximizes windows without hiding bars and shows tabs for all windows
in the layout.

I developed this for my own needs and currently do not have time to make it
"complete". Feel free to let me know (for example, by [opening an Issue]) and
fork the repository if you want to develop it further.

**Note:** The code has been updated for Qtile >= 0.23.0.
For older Qtile releases, try the `v0.22` branch.

[opening an Issue]: https://github.com/hanschen/qtile_tabbed/issues


Features
--------

- Show tabs at the top or bottom.
- Differently colored tabs for active, inactive, and urgent windows.
- Option to hide tabs if there is only one window.


Usage
-----

Copy or link the `tabbed.py` file to your qtile config directory, then import
the layout to your `config.py` file:

```python
from tabbed import Tabbed

...

layouts = [
    Tabbed(
        (options)
    ),
    ...
]

```


Options
-------

| Option            | Description                                       | Default   |
| ----------------- | ------------------------------------------------- | --------- |
| bg_color          | Background color of tab bar                       | "000000"  |
| active_fg         | Foreground color of active tab                    | "ffffff"  |
| active_bg         | Background color of active tab                    | "000080"  |
| urgent_fg         | Foreground color of urgent tab                    | "ffffff"  |
| urgent_bg         | Background color of urgent tab                    | "ff0000"  |
| inactive_fg       | Foreground color of inactive tab                  | "ffffff"  |
| inactive_bg       | Background color of inactive tab                  | "606060"  |
| rounded_tabs      | Draw tabs rounded                                 | False     |
| padding_y         | Top and bottom padding for tab label              | 2         |
| hspace            | Space between tabs                                | 2         |
| font              | Font                                              | "sans"    |
| fontsize          | Font pixel size                                   | 14        |
| fontshadow        | Font shadow color, default is None (no shadow)    | None      |
| bar_height        | Height of tab bar                                 | 24        |
| place_bottom      | Place tab bar at the bottom instead of top        | False     |
| show_single_tab   | Show tabs if there is only a single tab           | True      |


Missing features
----------------

- Sideway tabs (left or right).


Credits
-------

The code is partially based on the TreeTab layout in Qtile.
