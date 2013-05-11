[triangle.less](https://github.com/theinternetismadeofcats/triangle.less)
=============
Create simple triangular shapes in LESS.

Usage
-----

```html
<span class="point-right"></span> Here !
```

```less
.point-right
{
  .triangle(right, 20px, 15px, #222222);
  margin-right: 1em;
}
```

General use :

```less
//.triangle( @direction, @width, @height, @color )
.triangle(SW, 50px, 50px, #FF0000);
.triangle(N, 20%, 10%, black);
.triangle(up-left, 0.5em, 0.5em, rgb(128, 128, 128) );

//etc.
```

Where `@direction` can be any of the following :
```
N, NE, E, SE, S, SW, W, NW
up, up-right, right, down-right, down, down-left, left, up-left
```

Keep in mind that the element you use cannot have any content (this is enforced by `content: "";`). Think of it as if it was a separate image, not something you can put markup in.


How it works
------------
It uses the well-known CSS border trick, where you create a 0-width, 0-height element with a ridiculously large border on one or two sides, which ends up looking like a triangle, due to the way the browser handles the transition between adjacent borders.
This small LESS mixin hides the opaque border settings from you and lets you define triangles of any size and color in 8 directions.

You can use it to replace numerous small images for next/previous/play buttons, back-to-the-top buttons, dropdown lists, bullet points, beveled corners, etc.

License
-------

triangle.less is released under the [MIT license](http://opensource.org/licenses/mit-license.php).

(c) Pierre Boyer 2013