# inclusioneconomicsscheme

---

The *Inclusion Economics* Stata scheme provides a quick set of options for modern-looking graphs from Stata using *Inclusion Economics* colors.
The scheme is intended for use by the research team of *Inclusion Economics* when designing visualization for presentations and social media.
There are no restrictions on its use.

Two schemes are provided:

| Scheme  | Description                                      |
| ------- | ------------------------------------------------ |
| **ie**  | Three/four-color scheme using core brand palette |
| **ie2** | Six-color scheme using expanded palette          |

**Note:** Refer to Colors for more on **ie** and **ie2**.

**Important:** Refer to Fonts for setting up fonts.

## Installing via *ssc*

The *Inclusion Economics* scheme is available for download via ssc:

```stata
ssc install inclusioneconomicsscheme
```

## Usage

Specify the scheme at the start of a do-file:

```stata
set scheme ie
```

*or*:

```stata
set scheme ie2
```

Alternatively, specify the scheme for an individual graph:

```stata
sysuse auto
twoway  (scatter price mpg if foreign == 0) ///
		(scatter price mpg if foreign == 1), scheme(ie)
```

Alternatively, specify the default scheme at the command prompt:

```stata
set scheme ie, permanently
```

**Note:** Once installed, you will need to restart Stata for the scheme to be recognized.

## Colors

*Inclusion Economics* colors are navy, orange, blue, and beige.
The scheme **ie** uses these colors for bar, pie, and area graphs.
For other graph types, beige is omitted for readability.

- ![#00356B](https://via.placeholder.com/15/00356B/000000?text=+) `#00356B` IE navy
- ![#8CA1BC](https://via.placeholder.com/15/8CA1BC/000000?text=+) `#8CA1BC` IE blue
- ![#CE8769](https://via.placeholder.com/15/CE8769/000000?text=+) `#CE8769` IE orange
- ![#D3CFC3](https://via.placeholder.com/15/D3CFC3/000000?text=+) `#D3CFC3` IE beige

When more than three or four colors are required, you may specify the scheme **ie2**, which has an extended palette of six colors.

- ![#8CA1BC](https://via.placeholder.com/15/8CA1BC/000000?text=+) `#8CA1BC` IE blue
- ![#CE8769](https://via.placeholder.com/15/CE8769/000000?text=+) `#CE8769` IE orange
- ![#7CC0AC](https://via.placeholder.com/15/7CC0AC/000000?text=+) `#7CC0AC` IE teal
- ![#CA7294](https://via.placeholder.com/15/CA7294/000000?text=+) `#CA7294` IE magenta
- ![#E7CA55](https://via.placeholder.com/15/E7CA55/000000?text=+) `#E7CA55` IE yellow
- ![#9ECF6E](https://via.placeholder.com/15/9ECF6E/000000?text=+) `#9ECF6E` IE green

If these colors are not suitable, you may manually override them.
They should appear as the first eight colors in color menus of the Graph Editor, and they may also be specified directly in do-files.
The colors are named **ienavy**, **iebeige**, **ieblue**, **ieorange**, **ieteal**, **iemagenta**, **ieyellow**, **iegreen**.
(In menus, they appear as "IE navy", etc.)

## Fonts

The *Inclusion Economics* scheme is intended to be used with *Inclusion Economics* official fonts, [Montserrat](https://fonts.google.com/specimen/Montserrat) and [Lora](https://fonts.google.com/specimen/Lora), which must be independently downloaded and installed from Google Fonts.
Once they are installed, you can use **iefonts** to configure them.
See **iefonts** for more detail.

## Attribution

The *Inclusion Economics* scheme was written by Nils Enevoldsen. Bugs can be
reported via the repository at [Github](https://github.com/NilsEnevoldsen/inclusioneconomicsscheme).
Questions can be directed to nils [at] wlonk [dot] com. 

This scheme is a fork of the Yale scheme, written by Aaron Wolf, which can be
found at https://github.com/aarondwolf/yalescheme.

This scheme used the user-written scheme *cleanplots* as a base, with
alterations made to reflect the colors of Inclusion Economics and stylistic
preferences. *cleanplots* was created by Trenton Mize, and documentation can be
found at https://www.trentonmize.com/software/cleanplots. *cleanplots* was
itself influenced by Daniel Bischof's very excellent *plotplain* scheme,
documentation for which can be found at https://www.stata-journal.com/article.html?article=gr0070. 

To make the six-color **ie2** palette, IE orange and IE blue were used as a base, and off-brand colors were added,
roughly based on the [ColorBrewer2 Qualitative 6-Class Set2 palette](https://colorbrewer2.org/#type=qualitative&scheme=Set2&n=6).
ColorBrewer2 is made by Cynthia Brewer and Mark Harrower.
