# showcar-carousel

This module provides a easy to use carousel.

## Usage

For an example usage of the carousel, have a look inside the examples directory.
Just run the following command in root of the carousel library

```
$> npm start
```

This will open a small express server on your local machine where you can see the running example
[http://localhost:8080](http://localhost:8080)


### HTML Code

The whole carousel is defined by an `as24-carousel` element. 
Each item needs to be wrapped inside a `as24-carousel-item` element.
See the following example below:

```html
<as24-carousel>

    <as24-carousel-item>
      <a href="javascript:void(0);">
        <div class="as24-carousel-image-container">
            <img data-src="http://placehold.it/320x240?text=1,320x240"
                 src=""
                 alt="">
        </div>
        <div class="as24-carousel-description">
            <h5>Headline</h5>
            <p>Content</p>
        </div>
      </a>
    </as24-carousel-item>
    ...

</as24-carousel>
```

#### lazy loading
 For better performance it is possible to lazy load images. Therefor just replace
 the `src` attribute of your `img` with an `data-src` attribute.

#### CSS Styling ( Changing the image aspect ratio)

Currently the default style is set to support 4:3 images if the carousel uses an different format please overwrite "padding-bottom"
In order to change the aspect ratio of the images in the carousel add the following to you implementation.

```css
  // CAROUSEL ITEM
  as24-carousel-item > .carousel-image-container {
    // Aspect ratio of the image ( 100% width / 75% height = 1.333 )
    padding-bottom: 75%;
  }
```

### JS Interface

If you need to change the width of the carousel dynamically, you can call the ``redraw()`` method, to force the carousel to recalculate its sizings and positionings.
Note: Window resizing is included out of the box

```
document.getElementById('carousel-example').redraw()
```

## Installation

### How to install:

  To install showcar-carousel within your project use npm.

  ```
  npm install --save git@github.com:AutoScout24/showcar-carousel.git
  ```

  Afterwards you need to add the css and js to your page.

  ```html
  <link rel="stylesheet" href="../dist/showcar-carousel.css">
  ```

  ```html
  <script src="../dist/showcar-carousel.js"></script>
  ```

  showcar-carousel has no further dependencies.

***

## Contributing

### How to contribute:

  Fork this repository and `git clone` your fork. Then `npm install` the required dependencies.

#### Contribute

  Save your changes and run `npm build`.

  Commit your code _and_ the compiled libraries in _./dist_. Then create a pull-request.

## License

MIT License

***

