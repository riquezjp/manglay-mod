This is designed to be used with Archcraft 2026-08-01 MangoWC premium.

It will show the current layout name on the waybar such as [DWINDLE] or [TILE] in a matching style.

1 - Put the file `mango-layout` in `~/.config/mango/scripts`

2 - Make executable

3 - Add this module to `~/.config/mango/waybar/modules`
```
 // mango-layout
    "custom/mango-layout": {
		"exec": "~/.config/mango/scripts/mango-layout",
		"interval": 1,
		"format": "{}",
		"tooltip": false
	}
```
  4 - Add the module to your waybar in `~/.config/mango/waybar/config` by adding: `"custom/mango-layout"`

  example: 
```
  "modules-center": [ "ext/workspaces", "custom/mango-layout" ],
```
  5 - Add `#custom-mango-layout` to the CSS file `~/.config/mango/waybar/style.css`
  Open the CSS file, scroll all the way to the bottom & add it to the common style.

  example: (I added it here as the first #id in the list)
```
  /** ********** Common style ********** **/
#custom-mango-layout,
#pulseaudio,
#backlight,
#bluetooth, 
#network,
#battery,
#clock {
	background-color: @background-alt1;
	color: @foreground;
	border-radius: 8px;
	padding: 2px 12px;
	margin: 6px 0px ;
}
```
  6 - That's all. logout / login

  ISSUES:
  If the waybar doesnt load as normal, you made an error in code. Check.
  Step 3 - make sure you didnt miss a comma before of after the block of code, its an easy mistake to make.

  
