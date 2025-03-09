# uom_sphinx_wagtail_theme
University of Manchester Sphinx theme. 

This has added University of Manchester branding/colouring. It has also added an alternative font mode, where the text is displayed using OpenDyslexic rather than the default Roboto.

It is intended to be included as a Git submodule in other Sphinx projects. 

The alternative font mode is somewhat hard coded, particularly for the font-name variable. Moreover, the wagtail theme don't actually use pygment for code highlighting - it has a fixed static colour scheme. To get the code changing we thus just hard code over this hard coding! 
  $ pygmentize -S default -f html -a .highlight > pygments-theme-light.css
  $ pygmentize -S monokai -f html -a .highlight > pygments-theme-dark.css
were used to generate css files. These are then just loaded over the default wagtail pygments.css file. Note that the "default" colour scheme don't include all of the classes that are in the wagtail pygments.css, and so these classes were added in by hand so that our css file takes precedence in every case.

This is a modified version of the [sphinx-wagtail-theme]: https://github.com/wagtail/sphinx-wagtail-theme, which is released, modified, and included here under an MIT license. 

OpenDyslexic and OpenDyslexicMono fonts are included from [OpenDyslexic]: https://opendyslexic.org/,  released and included here under an SIL Open Font License v1.1.
