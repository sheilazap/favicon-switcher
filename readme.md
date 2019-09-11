# Favicon Switcher

[Live preview](https://rumkin.github.io/favicon-switcher)

![Light mode favicon example](assets/example-light.png)
![Dark mode favicon example](assets/example-dark.png)

Switches site's favicon by matching media queries. It could be used for
light/dark mode switching. Due to browsers don't support all Media Query
features in link tag, this module fixes it.

## Usage

Script doesn't require any setup or configuration and works like a polyfill.
The example below shows how to make dark/light mode icon switching.

Use the main library to automatically turn icon switching on:

```html
<script src="https://unpkg.com/favicon-switcher@1.0.0/dist/index.js" crossorigin="anonymous" type="application/javascript"></script>
```

If you need more control to turn switching on and off use one of the next
module:

### UMD

Use with UMD:

```html
<script src="https://unpkg.com/favicon-switcher@1.0.0/dist/index.umd.js" crossorigin="anonymous" type="application/javascript"></script>
<script>faviconSwitcher()</script>
```

### ESM

Use as ES module:

```html
<script type="module" language="javascript">
  import initSwitcher from 'https://unpkg.com/favicon-switcher@1.0.0/dist/index.esm.js'

  // Subscribe to media queries changing events
  const unsubscribe = initSwitcher()
  // Unsubscribe later on some condition. For example on page navigation.
  unsubscribe()
</script>
```

## Complete example

```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <link rel="icon" media="(prefers-color-scheme:dark)" href="favicon-dark.png" type="image/png" />
    <link rel="icon" media="(prefers-color-scheme:light)" href="favicon-light.png" type="image/png" />
    <script src="https://unpkg.com/favicon-switcher@1.0.0/dist/index.js" crossorigin="anonymous" type="application/javascript"></script>
  </head>
  <body></body>
</html>
```


## License

MIT © [Rumkin](https://rumk.in)
