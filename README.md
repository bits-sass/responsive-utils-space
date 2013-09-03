# Bits.sass utilities: responsive space

Responsive superset of space utilities.

See [Bits.sass utils-space](https://github.com/bits-sass/utils-space) for more about
original utilities.

Read more about [Bits.sass toolkit](https://github.com/bits-sass/bits.sass).

## Installation

* __Bower:__ `bower install --save bits-sass-responsive-utils-space`
* __Download:__ [zip](https://github.com/bits-sass/responsive-utils-space/zipball/master), [tar.gz](https://github.com/bits-sass/responsive-utils-space/tarball/master)
* __Git:__ `git clone https://github.com/bits-sass/responsive-utils-space.git`

## Available SASS variables

* `bits-utils-ns` - utilities namespace, defaults to 'bits-'

### Margin collapsing

* `bits-responsive-space-collapse-include` - whether to include these utils, defaults to __false__
* `bits-responsive-space-collapse-margin` - size of margin top / bottom that should be collapsed

### Spacing

* `bits-responsive-space-spacing-include` - whether to include these utils, defaults to __false__
* `bits-responsive-space-spacing-directions` - specifies list of generated `<D>` directions
* `bits-responsive-space-spacing-sizes` - specifies list of generated `<s>` sizes

### Gutters

* `bits-responsive-space-gutter-include` - whether to include these utils, defaults to __true__
* `bits-responsive-space-gutter-supported-children` - specifies list of supported children
   that should have a gutter inbetween
* `bits-responsive-space-gutter-types` - specifies list of generated `<T>` types
* `bits-responsive-space-gutter-sizes` - specifies list of generated `<s>` sizes

### Stretching

* `bits-responsive-space-stretch-include` - whether to include these utils, defaults to __false__
* `bits-responsive-space-stretch-types` - specifies list of generated `<T>` types
* `bits-responsive-space-stretch-sizes` - specifies list of generated `<s>` sizes

## Available utility classes

### Margin collapsing

* `v[n]-u-collapseTop` - collapse first child's top margin on `n` breakpoint
* `v[n]-u-collapseBottom` - collapse last child's bottom margin on `n` breakpoint

### Spacing

* `v[n]-u-margin<D><s>` (adjustable) - margin of size `s` in the direction `D` on `n` breakpoint
* `v[n]-u-padding<D><s>` (adjustable) - padding of size `s` in the direction `D` on `n` breakpoint

### Gutters

* `v[n]-u-gutter<T><s>` (adjustable) - gutter of size `s` and type `T` on `n` breakpoint

### Stretching

* `v[n]-u-stretch<T><s>` (adjustable) - stretching of size `s` and type `T` on `n` breakpoint

## Usage

Only utilities that are enable by default are 'gutters', because they are the
most used ones. You should avoid using `u-[margin|padding]Ds`, use a responsive
component instead.

List of items with a medium vertical gutter. On `v4` breakpoint, the gutter
becomes large.

```html
<ul class="u-gutterVm v4-u-gutterVl">
  <li class="u-gutter-item">…</li>
  <li class="u-gutter-item">…</li>
  <li class="u-gutter-item">…</li>
  <li class="u-gutter-item">…</li>
</ul>
```

Apply gutter on `v2` breakpoint only.

```html
<ul class="v2-u-gutterVm">
  <li class="v2-u-gutter-item">…</li>
  <li class="v2-u-gutter-item">…</li>
  <li class="v2-u-gutter-item">…</li>
  <li class="v2-u-gutter-item">…</li>
</ul>
```

Grid that has a small gutter by default. On `v4` breakpoint, the gutter changes to
medium and on `v7` it becomes large.

```html
<div class="Grid u-gutterHs v4-u-gutterHm v7-u-gutterHl">
  <div class="Grid-cell">
    …
  </div>
  <div class="Grid-cell">
    …
  </div>
</div>
```

N.B. You need to add `Grid-cell` to
`bits-responsive-space-gutter-supported-children` list.

## Requirements

* Sass 3.2+

## Browser support

* Google Chrome (latest)
* Opera (latest)
* Firefox 4+
* Safari 5+
* Internet Explorer 9+ (IE 8 requires a build step)