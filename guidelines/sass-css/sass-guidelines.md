# Sass guidelines

I will list here the guidelines I use for my sass files.

These good practices are inspired by guidelines used and created at work.

I have used them in many situations, but as each project is different, they can vary from one project to another.

## Folder architecture

* The `stylesheets` folder will always have the same architecture. As I use the [Atomic Design Methodology](http://bradfrost.com/blog/post/atomic-web-design/), I won't have a Sass file for each page.

    ```ruby
    |
    |  # Global folder
    |- styesheets/
    |    |
    |    |
    |    |
    |    |
    |    |  # The folder to group the atomic components
    |    |- components/
    |    |    |
    |    |    |  # Basic building blocks. (Atoms)
    |    |    |- atoms/
    |    |    |    |
    |    |    |    |- _typography.sass
    |    |    |    |- _link.sass
    |    |    |    |- _button.sass
    |    |    |    |- _alert.sass
    |    |    |    |- _image.sass
    |    |    |    |- ...
    |    |    |
    |    |    |
    |    |    |  # Groups of atoms bonded together. (molecules)
    |    |    |- molecules/
    |    |    |    |
    |    |    |    |- _modal.sass
    |    |    |    |- _card.sass
    |    |    |    |- _slider.sass
    |    |    |    |- _searchbar.sass
    |    |    |    |- _hero.sass
    |    |    |    |- ...
    |    |    |
    |    |    |  # Groups of molecules stitched together to form pages. (organisms)
    |    |    |- organisms/
    |    |         |
    |    |         |- _wrapper.sass
    |    |         |- _section.sass
    |    |         |- _sidebar.sass
    |    |         |- ...
    |    |
    |    |
    |    |
    |    |
    |    |  # Helpers
    |    |- helpers/
    |    |    |
    |    |    |- _mixins.sass
    |    |    |- _navigator.sass
    |    |    |- _variables.sass
    |    |    |- ...
    |    |
    |    |
    |    |
    |    |
    |    |  # Default layout files
    |    |- layout/
    |    |    |- _base.sass             # global elements: body, html ...
    |    |    |- _header.sass
    |    |    |- _footer.sass
    |    |    |- _fonts.sass            # Local fonts
    |    |    |- ...
    |    |
    |    |
    |    |
    |    |
    |    |  # The folder to group responsive files.
    |    |- responsive/
    |    |    |
    |    |    |
    |    |    |  # Responsive for atomic components.
    |    |    |  # I add 'responsive' before the component name to avoid confusion with the base file.
    |    |    |- responsive-components/
    |    |    |    |
    |    |    |    |- responsive-atoms/
    |    |    |    |    |- _responsive-typography.sass
    |    |    |    |    |- _responsive-link.sass
    |    |    |    |    |- _responsive-button.sass
    |    |    |    |    |- _responsive-alert.sass
    |    |    |    |    |- _responsive-image.sass
    |    |    |    |    |- ...
    |    |    |    |
    |    |    |    |- responsive-molecules/
    |    |    |    |    |- _responsive-modal.sass
    |    |    |    |    |- _responsive-card.sass
    |    |    |    |    |- _responsive-slider.sass
    |    |    |    |    |- _responsive-searchbar.sass
    |    |    |    |    |- _responsive-hero.sass
    |    |    |    |    |- ...
    |    |    |    |
    |    |    |    |- responsive-organisms/
    |    |    |    |    |- _responsive-wrapper.sass
    |    |    |    |    |- _responsive-section.sass
    |    |    |    |    |- _responsive-sidebar.sass
    |    |    |    |    |- ...
    |    |    |
    |    |    |
    |    |    |  # Responsive for layout.
    |    |    |- responsive-layout/
    |    |    |    |
    |    |    |    |- _responsive-footer.sass
    |    |    |    |- _responsive-header.sass
    |    |    |    |- _responsive-base.sass
    |    |    |    |- ...
    |    |
    |    |
    |    |
    |    |
    |    |  # The folder for external libraries
    |    |- vendors/
    |    |    |
    |    |    |- bootstrap.min.xxx
    |    |    |- select2.xxx
    |    |    |- slick.xxx
    |    |    |- ...
    |    |
    |    |
    |    |
    |    |
    |    | # Call every Sass partials
    |    |- main.sass
    |
    ```

## Syntax and Formatting

* The goal is to have a code that always look similar from a file to another.

    * 70 character max-wide columns.
    * two (2) space indents, no tabs.
    * multi-line Sass.

## Global file organization

* I always try to make my files look familiar, so it's important to keep the same file organiszation.

  * ### File title
    * A Sass file always begin with a clear title.
    ```sass
    // PROJECT NAME - FOLDER file.sass - Author
    // --------------------------------------------------------
    ```

    <br/>
  * ### Maximum file size
    * The size of a file should never exceed 250 lines.
    * As needed, separate the file into two different files.

    <br/>
  * ### Table of contents
    * As I rarely work with big files, I do not use often a tabe of contents.
    * But in some case, it can be usefull to create a table of contents to list the main section of the file.
    ```sass
    /**
     * TABLE OF CONTENTS
     *
     * DEFAULT INPUT STYLE
     * Just write here the summury of what's inside.
     *
     * INPUT COLOR
     * Just write here the summury of what's inside.
     *
     * INPUT SIZE
     * Just write here the summury of what's inside.
     *
     * INPUT SHAPE
     * Just write here the summury of what's inside.
     *
     * INPUT ICON
     * Just write here the summury of what's inside.
     */
    ```

    <br/>

## Commenting & spacing



