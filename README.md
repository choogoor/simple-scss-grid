# Simple SASS Grid

Simple SASS grid is a lightweight grid built with idea to be smart and easy to use.

## Usage

All you have to do is to copy *sass* folder content to your stylesheet folder and import `_grid.scss` file into your main stylesheet file.

```scss
@import 'grid';
```

### Structure

All columns are contained within columns container which lays down inside row wrapper with certain `max-width`. You can easily set your own `max-width` in config file. HTML markup should look like this one below (Just be sure that this one use default naming for *breakpoints* from [config file](#config)).

```HTML
<div class="row">
  <div class="columns">
    <div class="column-12 column-mobile-4"> ... </div>
    <div class="column-12 column-mobile-8"> ... </div>
  </div>
</div>
```

### Options

There is a few options within this grid, which can be applied with *classes*.

#### Reverse Grid `.reverse`

Reverse order of your columns opposite to your html.

```HTML
<div class="row">
  <div class="columns reverse">
    <div class="column-12 column-mobile-4"> ... </div>
    <div class="column-12 column-mobile-8"> ... </div>
  </div>
</div>
```

#### No Gutters `.no-gutters`

Remove gutters between the columns.

```HTML
<div class="row">
  <div class="columns no-gutters">
    <div class="column-12 column-mobile-4"> ... </div>
    <div class="column-12 column-mobile-8"> ... </div>
  </div>
</div>
```

#### Align Center `.align-center`

Vertically center your columns.

```HTML
<div class="row">
  <div class="columns align-center">
    <div class="column-12 column-mobile-4"> ... </div>
    <div class="column-12 column-mobile-8"> ... </div>
  </div>
</div>
```

#### Hide columns

If you want for some reason to hide column for certain breakpoint you could apply `.column-...-0` class.

```HTML
<div class="row">
  <div class="columns align-center">
    <div class="column-12 column-mobile-0"> ... </div>
    <div class="column-0 column-mobile-12"> ... </div>
  </div>
</div>
```

### Config

There are the few options that you can edit, such as:
- `$grid-media-queries` - Breakpoints for your responsive grid. Both *key* and the *value*, as well as number of breakpoints are up to you.
- `$grid-columns` - Number of grid columns.
- `$grid-max-width` - `.row` container `max-width` value.
- `$grid-narrow-width` - For some pages you need narrower container (blog post text for example), so this variable contain `max-width` value for it.
- `$grid-breakpoints` - You can use your own breakpoints if you have it (You use custom breakpoint mixin for example).

```scss
$grid-media-queries: (
  mobile: 480px,
  tablet: 980px,
  laptop: 1280px,
  desktop: 1440px
);

$grid-columns: 12 !default;
$grid-gutter-width: 1.5625rem !default;
$grid-max-width: 1280px !default;
$grid-narrow-width: 720px !default;
$grid-breakpoints: $grid-media-queries !default;
```

## Licence
Licensed under the MIT license.
