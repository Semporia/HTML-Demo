# prefers-color-scheme

```
If you have set privacy.resistFingerprinting to true, prefers-color-scheme preference is overridden to light.
Alternately, users can create the numeric preference ui.systemUsesDarkTheme to override the default behavior and return light (value: 0), dark (value: 1), or no-preference (value: 2). (Any other value causes Firefox to return light.)
```

The prefers-color-scheme CSS media feature is used to detect if the user has requested the system use a light or dark color theme.

### Syntax

* light
  Indicates that user has notified the system that they prefer an interface that has a light theme, or has not expressed an active preference.

* dark
  Indicates that user has notified the system that they prefer an interface that has a dark theme.

### Examples

  The elements below have an initial color theme. They can be further themed according to the user's color scheme preference.

### HTML

```
<div class="day">Day (initial)</div>
<div class="day light-scheme">Day (changes in light scheme)</div>
<div class="day dark-scheme">Day (changes in dark scheme)</div> <br>

<div class="night">Night (initial)</div>
<div class="night light-scheme">Night (changes in light scheme)</div>
<div class="night dark-scheme">Night (changes in dark scheme)</div>
```

### CSS

```
.day   { background: #eee; color: black; }
.night { background: #333; color: white; }

@media (prefers-color-scheme: dark) {
  .day.dark-scheme   { background:  #333; color: white; }
  .night.dark-scheme { background: black; color:  #ddd; }
}

@media (prefers-color-scheme: light) {
  .day.light-scheme   { background: white; color:  #555; }
  .night.light-scheme { background:  #eee; color: black; }
}

.day, .night {display: inline-block; padding: 1em; width: 7em; height: 2em; vertical-align: middle; }
```


### Result

```html
<!DOCTYPE html>
<html>

<head>
  <meta http-equiv="content-type" content="text/html; charset=UTF-8">
  <meta charset="utf-8">
  <style type="text/css">
  body {
    padding: 0;
    margin: 0;
  }

  svg:not(:root) {
    display: block;
  }

  .playable-code {
    background-color: #f4f7f8;
    border: none;
    border-left: 6px solid #558abb;
    border-width: medium medium medium 6px;
    color: #4d4e53;
    height: 100px;
    width: 90%;
    padding: 10px 10px 0;
  }

  .playable-canvas {
    border: 1px solid #4d4e53;
    border-radius: 2px;
  }

  .playable-buttons {
    text-align: right;
    width: 90%;
    padding: 5px 10px 5px 26px;
  }
  </style>
  <style type="text/css">
  .day {
    background: #eee;
    color: black;
  }

  .night {
    background: #333;
    color: white;
  }

  @media (prefers-color-scheme: dark) {
    .day.dark-scheme {
      background: #333;
      color: white;
    }

    .night.dark-scheme {
      background: black;
      color: #ddd;
    }
  }

  @media (prefers-color-scheme: light) {
    .day.light-scheme {
      background: white;
      color: #555;
    }

    .night.light-scheme {
      background: #eee;
      color: black;
    }
  }

  .day, .night {
    display: inline-block;
    padding: 1em;
    width: 7em;
    height: 2em;
    vertical-align: middle;
  }
  </style>
  <title>prefers-color-scheme - Examples - code sample</title>
</head>

<body>
  <div class="day">Day (initial)</div>
  <div class="day light-scheme">Day (changes in light scheme)</div>
  <div class="day dark-scheme">Day (changes in dark scheme)</div> <br>
  <div class="night">Night (initial)</div>
  <div class="night light-scheme">Night (changes in light scheme)</div>
  <div class="night dark-scheme">Night (changes in dark scheme)</div>
</body>

</html>
```
