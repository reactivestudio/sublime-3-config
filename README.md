# Sublime Text 3 Drupal Development Setup

Optimized to use with Drupal, JavaScript, React and Material Design

# 1. Getting Started

Download and install [Sublime3](http://www.sublimetext.com/3) for your operating system.

# 2. Install Packages 

## Package Manager

In order to easily install these 3rd party packages, you will first need to navigate to the [Package Control installer](https://sublime.wbond.net/installation#st3) and **copy** the code underneath the Sublime3 tab, which looks like:

```python
import urllib.request,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

Open the menu `View > Show Console` and a console will open at the bottom. **Paste** the code which you copied in the previous step and press enter. Sublime3 will then install the Package Control manager for you.

## HTML

- [Emmet](https://packagecontrol.io/packages/Emmet) - A must for working fast with HTML/CSS
- [Tag](https://packagecontrol.io/packages/Tag) - Auto closes tags and lints for matched tags
- [HTML-CSS-JS Prettify](https://packagecontrol.io/packages/HTML-CSS-JS%20Prettify) - HTML/CSS/JavaScript formatter
 
## CSS/SASS/SCSS
- [Gutter Color](https://packagecontrol.io/packages/Gutter%20Color) - CSS colors in gutter
- [SASS](https://packagecontrol.io/packages/SASS) - SASS syntax highlighting
- [SCSS](https://packagecontrol.io/packages/SCSS) - SCSS syntax highlighting
- [SASS Beautify](https://packagecontrol.io/packages/SassBeautify) - A Sublime Text plugin that beautifies Sass files

## Drupal Specific Packages

- [Drupal](https://sublime.wbond.net/packages/Drupal)
- [Drupal Completions](https://packagecontrol.io/packages/Drupal%20Completions)
- [Drupal Project Autocomplete](https://packagecontrol.io/packages/Drupal%20Project%20Autocomplete)
- [Goto Drupal API](https://sublime.wbond.net/packages/Goto%20Drupal%20API)

## Autocomplete
- [All Autocomplete](https://packagecontrol.io/packages/Gutter%20Color) - CSS colors in gutter
- [Advanced New File](https://packagecontrol.io/packages/AdvancedNewFile) - File creation plugin
- [Auto Semi-Colon](https://packagecontrol.io/packages/Auto%20Semi-Colon) - Automatically moves a semi-colon to the outside of the last bracket when pressed inside
- [Sublime ​Code ​Intel](https://packagecontrol.io/packages/SublimeCodeIntel) - Full-featured code intelligence and smart autocomplete engine

## Coding Standards and Helpers Packages
- [DocBlockr](https://sublime.wbond.net/packages/DocBlockr) -
- [Alignment](https://packagecontrol.io/packages/Alignment) - Easy alignment of multiple selections and multi-line selections
- [Bracket​ Highlighter](https://packagecontrol.io/packages/Bracket​Highlighter) - Bracket and tag highlighter
- [Sublime​Linter](https://packagecontrol.io/packages/Sublime​Linter) - Interactive code linting framework
- [Sublime​Linter-annotations](https://packagecontrol.io/packages/Sublime​Linter-annotations) - SublimeLinter 3 plugin that marks annotations such as TODO, FIXME, etc
- [Trimmer](https://packagecontrol.io/packages/Trimmer) - A Sublime Text plug-in for cleaning up whitespace

## Syntax Helpers
- [Apply​Syntax](https://packagecontrol.io/packages/Apply​Syntax) - Syntax detector
- [NGINX](https://packagecontrol.io/packages/nginx) - Improved syntax support for Nginx configuration files

## Version Control
- [Git​Savvy](https://packagecontrol.io/packages/GitSavvy) - Full git and GitHub integration
- [Git​Gutter](https://packagecontrol.io/packages/GitGutter) - A Sublime Text 2/3 plugin to see git diff in gutter
- [Git​Status](https://packagecontrol.io/packages/Git​Status) - Monitoring changed files and status of the repository

## Theme Package

- [Theme - Materialize](https://github.com/saadq/Materialize)
![Material Theme](https://raw.githubusercontent.com/saadq/Materialize/master/screenshots/material-spacegray.png)

Open the menu `Preferences > Settings - User` and **paste** the following and **Save**

```json
{
  "color_scheme": "Packages/Materialize/schemes/Material Spacegray.tmTheme",
  "theme": "Material Spacegray.sublime-theme",
  "material_theme_accent_yellow": true,
  "material_theme_bold_tab": true,
  "material_theme_compact_panel": true,
  "material_theme_compact_sidebar": true,
  "material_theme_contrast_mode": true,
  "material_theme_disable_tree_indicator": true,
  "material_theme_small_statusbar": true,
  "material_theme_tabs_autowidth": true,
}
```
Add `Material Spacegray.sublime-theme` from this repo to `~/Users/admin/Library/Application Support/Sublime Text 3/Packages/User`

## Debugging Package

- [Xdebug Client](https://sublime.wbond.net/packages/Xdebug%20Client)

Be sure you add the `url` for browser debugging and `path_mapping` configuration for remote debugging to function in `Tools > XDebug > Settings > Settings - User`.

```json
{
  "url": "http://dev.example.com",
  "path_mapping": {
        "/absolute/path/to/file/on/server" : "/absolute/path/to/file/on/computer"
    }
}
```


# 4. User Settings

Configure Sublime3 formatting with common Drupal settings, such as 2 spaces for indents, an 80 character right boarder, etc:

Open the menu `Preferences > Settings - User` and **paste** the following and **Save**

```json
{
	"always_show_minimap_viewport": true,
	"bold_folder_labels": true,
	"caret_extra_bottom": 2,
	"caret_extra_top": 2,
	"caret_style": "smooth",
	"color_scheme": "Packages/Materialize/schemes/Material Spacegray.tmTheme",
	"convert_path": "/Applications/MAMP/Library/bin/convert",
	"default_line_ending": "unix",
	"drag_text": false,
	"draw_indent_guides": false,
	"draw_white_space": "all",
	"enable_tab_scrolling": false,
	"ensure_newline_at_eof_on_save": true,
	"fade_fold_buttons": false,
	"fallback_encoding": "UTF-8",
	"find_selected_text": true,
	"font_face": "Fira Code",
	"font_options":
	[
		"subpixel_antialias"
	],
	"font_size": 12,
	"highlight_line": false,
	"ignored_packages":
	[
		"Vintage"
	],
	"line_padding_bottom": 3,
	"line_padding_top": 3,
	"material_theme_accent_yellow": true,
	"material_theme_bold_tab": true,
	"material_theme_compact_panel": true,
	"material_theme_compact_sidebar": true,
	"material_theme_contrast_mode": true,
	"material_theme_disable_tree_indicator": true,
	"material_theme_small_statusbar": true,
	"material_theme_tabs_autowidth": true,
	"open_files_in_new_window": false,
	"rulers":
	[
		80
	],
	"shift_tab_unindent": true,
	"tab_size": 2,
	"theme": "Material Spacegray.sublime-theme",
	"translate_tabs_to_spaces": true,
	"trim_automatic_white_space": true,
	"trim_trailing_white_space_on_save": true,
	"use_tab_stops": true,
	"word_separators": "./\\()\"'-:,.;<>~!@#%^&*|+=[]{}`~_?",
	"word_wrap": true
}
```



# 5. Drupal PHP Settings
Open `~/Library/Application Support/Sublime Text 3/Packages/User/PHP.sublime-settings` **paste** the following and **Save**.

```json
{
  "extensions":
   [
     "inc",
     "profile",
     "module",
     "install"
   ]
}
```
	
