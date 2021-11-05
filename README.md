# CSS notes

## `-webkit-line-clamp`

- It allows limiting of the contents of a block container to the specified number of lines.
- It only works in combination with the `display` property set to `-webkit-box` or `-webkit-inline-box` and the `-webkit-box-orient` property set to `vertical`.
- In most cases you will also want to set `overflow` to `hidden`, otherwise the contents won't be clipped but an ellipsis will be shown after the specified number of lines.

```css
width: 300px;
display: -webkit-box; /* -webkit-inline-box; */
-webkit-box-orient: vertical;
-webkit-line-clamp: 3; /* none | <integer> */
overflow: hidden;
```

## Relative length units

- `em`, `%`: relative to parent element
- `rem`: relative to root element, browser
- `vw`: 1% of the viewport's width
- `vh`: 1% of the viewport's height

```css
.relative-length-units {
  font-size: 24px;
}
.relative-length-units .header {
  background-color: brown;
  color: white;
  font-size: 2em; /* 48px */
  padding: 1em 2rem; /* 48px 32px */
}
.relative-length-units .content {
  font-size: 2rem; /* 32px */
  padding: 1em 2rem; /* 32px 32px */
}

@media only screen and (max-width: 61.9rem) {
}
```
