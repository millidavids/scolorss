# SColorSS

Define a single color, `$sc-seed`, to generate multiple color schemes. Access the main color with the sass function `color('sc-primary', 'base')`. The following color themes can be substituted as the first argument in that color function to get each color in that theme. The number 1-3 refer to the different colors of the theme. The 0th color in each theme is the primary color `sc-primary.`

- Complement: `'sc-complement'`
- Split Complement: `'sc-s-complement-{1,2}'`
- Analogous: `'sc-analogous-{1,2}'`
- Triadic: `'sc-triadic-{1,2}'`
- Positive Tetradic: `'sc-p-tetradic-{1,2,3}'`
- Negative Tetradic: `'sc-n-tetradic-{1,2,3}'`
- Square: `'sc-square-{1,2,3}'`

All colors in all themes come with lightened and darkened variables in 10 degree increments from 10-90 percentages. To access these use the color function and change the second argument. Example: `color('sc-primary', 'lighten-20')`.

You can also access 30 degree increments on the color wheel individually by passing in the interval like so: `color('sc-interval-30', 'base')`. The only caveat to this is that if you, for instance, decide not to include the whole scolorss.scss file, and opt to just use one theme; that theme only imports the intervals that it uses. To get all intervals, import the entire scolor.scss file.

### Recognition

I would like to thank [Materialize][Materialize] for giving me the idea of the color function. I would also like to thank Wilson Page for the [sass-import-once][sass-import-once] sass mixin.

[sass-import-once]: https://github.com/wilsonpage/sass-import-once
[Materialize]: http://materializecss.com/
