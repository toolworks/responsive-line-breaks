# responsive-line-breaks
Responsive line breaks, implemented for Bootstrap in a LESS syntax.

# Usage
First of all, make sure the main LESS file is somewhere within your style sources:
```less
@import "./toolworks/responsive-line-breaks.less";
```

After you have your LESS styles compiled into CSS, you may use the generated classes as described below.

## Technique 1: Responsive `<br />`
This tecnique can be used in some sophisticated scenarios like with Bootstrap's `text-ribbon` class in its official themes. Place an HTML `<br class="rwd-break"/>` element inside your text block:
```html
<h1>
  A line break example,<br class="rwd-break"/> for you to try out.
</h1>
```
[Jade](http://jade-lang.com/) example (note the `|` character used to escape):
```jade
h1
  | A line break example,<br class="rwd-break"/> for you to try out.
```

## Technique 2: Responsive `<span>`
This technique is the recommended one. Break your text block into HTML `<span class="rwd-line">` sections:
```html
<h1 class="block-title">
  <span class="rwd-line">A line break example, </span>
  <span class="rwd-line">for you to try out.</span>
</h1>
```

[Jade](http://jade-lang.com/) example (note the space character ` ` after the comma `,`):
```jade
h1
  span.rwd-line A line break example, 
  span.rwd-line for you to try out.
```

## Variants
For both types of techniques, you may use the resolution-adjusted versions of classes: `rwd-xs-break`, `rwd-sm-line`, etc. The standard Bootstrap resolution [tag](http://getbootstrap.com/css/#grid-options) (`xs`, `sm`, `md`, `lg`) specifies the resolution category smaller and equal to which the break functionality is activated.

# Attribution
The tech is based on the original article by [Dan Mall](http://danielmall.com/articles/responsive-line-breaks). Both of his techniques are implemented.
