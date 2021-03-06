---
disableHtmlPreviews: true
previousText: 'Responsive Grid'
previousUrl: '/docs/layout/grid'
nextText: 'RTL Support'
nextUrl: '/docs/layout/rtl'
---

# CSS Utilities

Ionic provides a set of utility attributes that can be used on any element in order to modify the text, element placement or adjust the padding and margin.


## Text Modification

### Text Alignment

| Attribute         | Style Rule             | Description                                                                                                                                                         |
|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text-left`       | `text-align: left`     | The inline contents are aligned to the left edge of the line box.                                                                                                   |
| `text-right`      | `text-align: right`    | The inline contents are aligned to the right edge of the line box.                                                                                                  |
| `text-start`      | `text-align: start`    | The same as `text-left` if direction is left-to-right and `text-right` if direction is right-to-left.                                                                         |
| `text-end`        | `text-align: end`      | The same as `text-right` if direction is left-to-right and `text-left` if direction is right-to-left.                                                                         |
| `text-center`     | `text-align: center`   | The inline contents are centered within the line box.                                                                                                               |
| `text-justify`    | `text-align: justify`  | The inline contents are justified. Text should be spaced to line up its left and right edges to the left and right edges of the line box, except for the last line. |
| `text-wrap`       | `white-space: normal`  | Sequences of whitespace are collapsed. Newline characters in the source are handled as other whitespace. Breaks lines as necessary to fill line boxes.              |
| `text-nowrap`     | `white-space: nowrap`  | Collapses whitespace as for `normal`, but suppresses line breaks (text wrapping) within text.                                                                       |

<div class="preview-row">
  <div class="preview-col" text-left>
    <strong>text-left</strong><br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
  </div>
  <div class="preview-col" text-right>
    <strong>text-right</strong><br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
  </div>
  <div class="preview-col" text-center>
    <strong>text-center</strong><br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
  </div>
</div>
<div class="preview-row">
  <div class="preview-col" text-justify>
    <strong>text-justify</strong><br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
  </div>
  <div class="preview-col" text-wrap>
    <strong>text-wrap</strong><br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
  </div>
  <div class="preview-col" text-nowrap>
    <strong>text-nowrap</strong><br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
  </div>
</div>

<em>Note: the example above is shown with custom styling.</em>

```html
<div text-left>
  text-left
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
</div>
<div text-right>
  text-right
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
</div>
<div text-center>
  text-center
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
</div>
<div text-justify>
  text-justify
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
</div>
<div text-wrap>
  text-wrap
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
</div>
<div text-nowrap>
  text-nowrap
  Lorem ipsum dolor sit amet, consectetur adipiscing elit.
</div>
```


### Text Transformation

| Attribute         | Style Rule                   | Description                                                         |
|-------------------|------------------------------|---------------------------------------------------------------------|
| `text-uppercase`  | `text-transform: uppercase`  | Forces all characters to be converted to uppercase.                 |
| `text-lowercase`  | `text-transform: lowercase`  | Forces all characters to be converted to lowercase.                 |
| `text-capitalize` | `text-transform: capitalize` | Forces the first letter of each word to be converted to uppercase.  |

<div class="preview-row">
  <div class="preview-col" text-uppercase>
    <strong>text-uppercase</strong><br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
  </div>
  <div class="preview-col" text-lowercase>
    <strong>text-lowercase</strong><br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
  </div>
  <div class="preview-col" text-capitalize>
    <strong>text-capitalize</strong><br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
  </div>
</div>

<em>Note: the example above is shown with custom styling.</em>

```html
<div text-uppercase>
  text-uppercase
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
</div>
<div text-lowercase>
  text-lowercase
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
</div>
<div text-capitalize>
  text-capitalize
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
</div>
```

### Responsive Text Attributes

All of the text attributes listed above have additional attributes to modify the text based on the screen size. Instead of `text-` in each attribute, use `text-{breakpoint}-` to only use the attribute on specific screen sizes, where `{breakpoint}` is one of the defined breakpoints in the `--screen-breakpoints` variable.

The table below shows the default behavior, where `{modifier}` is any of the following: `left`, `right`, `start`, `end`, `center`, `justify`, `wrap`, `nowrap`, `uppercase`, `lowercase`, or `capitalize`, as they are described above.

| Attribute             | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
| `text-{modifier}`     | Applies the modifier to the element on all screen sizes.            |
| `text-sm-{modifier}`  | Applies the modifier to the element when `min-width: 576px`.        |
| `text-md-{modifier}`  | Applies the modifier to the element when `min-width: 768px`.        |
| `text-lg-{modifier}`  | Applies the modifier to the element when `min-width: 992px`.        |
| `text-xl-{modifier}`  | Applies the modifier to the element when `min-width: 1200px`.       |


## Element Placement

### Float Elements

The float CSS property specifies that an element should be placed along the left or right side of its container, where text and inline elements will wrap around it. This way, the element is taken from the normal flow of the web page, though still remaining a part of the flow, contrary to absolute positioning.

| Attribute     | Style Rule                      | Description                                                                                               |
|---------------|---------------------------------|-----------------------------------------------------------------------------------------------------------|
| `float-left`  | `float: left`                   | The element will float on the left side of its containing block.                                          |
| `float-right` | `float: right`                  | The element will float on the right side of its containing block.                                         |
| `float-start` | `float: left` / `float: right`  | The same as `float-left` if direction is left-to-right and `float-right` if direction is right-to-left.   |
| `float-end`   | `float: left` / `float: right`  | The same as `float-right` if direction is left-to-right and `float-left` if direction is right-to-left.   |

<div class="preview-row">
  <div class="preview-col" float-left>
    <strong>float-left</strong><br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
  </div>
  <div class="preview-col" float-right>
    <strong>float-right</strong><br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
  </div>
</div>

<em>Note: the example above is shown with custom styling.</em>

```html
<div float-left>
  <strong>float-left</strong><br>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
</div>
<div float-right>
  <strong>float-right</strong><br>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ac vehicula lorem.
</div>
```

### Responsive Float Attributes

All of the float attributes listed above have additional attributes to modify the float based on the screen size. Instead of `float-` in each attribute, use `float-{breakpoint}-` to only use the attribute on specific screen sizes, where `{breakpoint}` is one of the defined breakpoints in the `--screen-breakpoints` variable.
The table below shows the default behavior, where `{modifier}` is any of the following: `left`, `right`, `start`, or `end`, as they are described above.

| Attribute              | Description                                                         |
|------------------------|---------------------------------------------------------------------|
| `float-{modifier}`     | Applies the modifier to the element on all screen sizes.            |
| `float-sm-{modifier}`  | Applies the modifier to the element when `min-width: 576px`.        |
| `float-md-{modifier}`  | Applies the modifier to the element when `min-width: 768px`.        |
| `float-lg-{modifier}`  | Applies the modifier to the element when `min-width: 992px`.        |
| `float-xl-{modifier}`  | Applies the modifier to the element when `min-width: 1200px`.       |


## Content Space

### Element Padding

The padding attribute sets the padding area of an element. The padding area is the space between the content of the element and its border.

The default amount of `padding` to be applied is `16px` and is set by the `--content-padding` variable. Each mode can have a different value for padding by setting `--content-ios-padding`, or `--content-md-padding`. See [CSS Variables](../theming/css-variables) for more information on how to change these values.


| Attribute            | Style Rule               | Description                             |
|----------------------|--------------------------|-----------------------------------------|
| `padding`            | `padding: 16px`          | Applies padding to all sides.           |
| `padding-top`        | `padding-top: 16px`      | Applies padding to the top.             |
| `padding-left`       | `padding-left: 16px`     | Applies padding to the left.            |
| `padding-right`      | `padding-right: 16px`    | Applies padding to the right.           |
| `padding-bottom`     | `padding-bottom: 16px`   | Applies padding to the bottom.          |
| `padding-vertical`   | `padding: 16px 0`        | Applies padding to the top and botttom. |
| `padding-horizontal` | `padding: 0 16px`        | Applies padding to the left and right.  |
| `no-padding`         | `padding: 0`             | Applies no padding to all sides.        |


<div class="preview-row">
  <div class="preview-col padding-col" padding>
    padding
  </div>
  <div class="preview-col padding-col" padding-top>
    padding-top
  </div>
  <div class="preview-col padding-col" padding-left>
    padding-left
  </div>
  <div class="preview-col padding-col" padding-right>
    padding-right
  </div>
  <div class="preview-col padding-col" padding-bottom>
    padding-bottom
  </div>
  <div class="preview-col padding-col" padding-vertical>
    padding-vertical
  </div>
  <div class="preview-col padding-col" padding-horizontal>
    padding-horizontal
  </div>
  <div class="preview-col padding-col" no-padding>
    no-padding
  </div>
</div>

<em>Note: the example above is shown with custom styling to show the padding that gets applied in green.</em>

```html
<div padding>
  padding
</div>
<div padding-top>
  padding-top
</div>
<div padding-left>
  padding-left
</div>
<div padding-right>
  padding-right
</div>
<div padding-bottom>
  padding-bottom
</div>
<div padding-vertical>
  padding-vertical
</div>
<div padding-horizontal>
  padding-horizontal
</div>
<div no-padding>
  no-padding
</div>
```

### Element Margin

The margin area extends the border area with an empty area used to separate the element from its neighbors.

The default amount of `margin` to be applied is `16px` and is set by the `--content-margin` variable. Each mode can have a different value for margin by setting `--content-ios-margin`, or `--content-md-margin`. See [CSS Variables](../theming/css-variables) for more information on how to change these values.


| Attribute            | Style Rule               | Description                             |
|----------------------|--------------------------|-----------------------------------------|
| `margin`             | `margin: 16px`           | Applies margin to all sides.            |
| `margin-top`         | `margin-top: 16px`       | Applies margin to the top.              |
| `margin-left`        | `margin-left: 16px`      | Applies margin to the left.             |
| `margin-right`       | `margin-right: 16px`     | Applies margin to the right.            |
| `margin-bottom`      | `margin-bottom: 16px`    | Applies margin to the bottom.           |
| `margin-vertical`    | `margin: 16px 0`         | Applies margin to the top and botttom.  |
| `margin-horizontal`  | `margin: 0 16px`         | Applies margin to the left and right.   |
| `no-margin`          | `margin: 0`              | Applies no margin to all sides.         |

<!-- Little bit of faking it here, using padding attributes so we can show it with a background -->
<div class="preview-row">
  <div class="preview-col margin-col" padding>
    <div>margin</div>
  </div>
  <div class="preview-col margin-col" padding-top>
    <div>margin-top</div>
  </div>
  <div class="preview-col margin-col" padding-left>
    <div>margin-left</div>
  </div>
  <div class="preview-col margin-col" padding-right>
    <div>margin-right</div>
  </div>
  <div class="preview-col margin-col" padding-bottom>
    <div>margin-bottom</div>
  </div>
  <div class="preview-col margin-col" padding-vertical>
    <div>margin-vertical</div>
  </div>
  <div class="preview-col margin-col" padding-horizontal>
    <div>margin-horizontal</div>
  </div>
  <div class="preview-col margin-col" no-padding>
    <div>no-margin</div>
  </div>
</div>

<em>Note: the example above is shown with custom styling to show the margin that gets applied in orange.</em>

```html
<div margin>
  margin
</div>
<div margin-top>
  margin-top
</div>
<div margin-left>
  margin-left
</div>
<div margin-right>
  margin-right
</div>
<div margin-bottom>
  margin-bottom
</div>
<div margin-vertical>
  margin-vertical
</div>
<div margin-horizontal>
  margin-horizontal
</div>
<div no-margin>
  no-margin
</div>
```
