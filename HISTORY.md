# Unreleased

* [Fix] Will no longer try to load non-html files in the columns directory

# 1.1.1 // 2016-09-09

Fixed an issue with core column classes. Plus some handy debugging stuff!

* [New] `Omniboard::Column.reset_columns` allows you to wipe the global register of columns. Useful for unit testing.
* [New] `Omniboard::Column.reset_config` now takes the option `:all` to wipe all configuration fields.
* [Fix] The `config.rb` template file will now let you have projects that are not contained within folders.

# 1.1.0 // 2016-08-29

Add custom CSS to your omniboard.

* [New] You can now add custom CSS to your board. Any CSS in the file `custom.css` (inside your config file) will be included in the output HTML file. See the readme for more information.

# 1.0.1 // 2016-08-01

* [Fix] Fixing CDATA tags within javascript - allows me to parse as XHTML while keeping JS all good.
* [Fix] Improved display of column header numbers.

# 1.0.0 // 2016-07-08

Hopefully integrating all the little changes, bugfixes, and modifications that I've wanted to do for a while.

* [New] `Omniboard::document=` is available if you just want to set Omniboard's document variable by yourself without all that hassle of loading from file.
* [New] If your document has no fetcher, it's always considered to be at head.
* [New] Substantial changes to how groups work. You may now return any object from a `group_by` method, and use that object to sort your groups before displaying names. See the Readme for more information on how to use the updated groups.
* [New] You can now custom colour your groups! See the Readme for more information.
* [New] The column's `icon` methods may now return an array of `[icon, alt]`, for supplying popup information on icons.
* [New] You can add a "refresh" link to the top of the page using the `refresh_link` property inside `config`.
* [New] Setting `hide_dimmed` on a column will automatically hide dimmed projects on page load
* [New] Set project counts using the `display_project_counts` property on columns. Can be set to `all`, `active`, or `marked`.

# 0.4.0 // 2016-06-27

Updates galore! Well, some updates, anyway. While there are some larger underlying problems with the codebase, I've just been focussing on the notes of each project.

* [New] Project notes will now show basic styling (italics, bold, underline; better paragraphs).
* [New] Added some shiny CSS for the project details - notes and remaining tasks lists should be a bit sexier
* [New] Projects now show due and deferral dates (when appropriate) in the project overlay

# 0.3.3 // 2016-05-23

Wow, it's been some time, hasn't it? Let's add updates to this.

* [New] Omniboard works out when your document is out of date, or even when it's become detached from the head of your omnifocus database, and lets you know.
* [Fix] `Group` now has a default `light_colour` method - no more errors if you don't group your projects!


# 0.3.1 // 2016-02-13

* [Fix] Remove console.log() debugging in js functions
* [Fix] Previous change to hide/show code resulted in a non-functioning info overlay. Now fixed.

# 0.3.0 // 2016-02-12

* [New] You can now set a block property to `nil` to avoid running any block (including any defaults).

# 0.2.1 // 2016-02-09

* [Fix] Added `trollop` to list of runtime dependencies

# 0.2.0 // 2016-02-08

A number of updates around the board

* [New] Project groups will hide themselves if every child project has been hidden.
* [New] Added `Column#filter_button`, which allows you to add a button filtering out dimmed tasks.

# 0.1.0 // 2016-02-04

Hello, world!