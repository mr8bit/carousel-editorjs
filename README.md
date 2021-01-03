![](https://badgen.net/badge/Editor.js/v2.0/blue)

# Carousel Tool

Carousel/Gallery Block for the [Editor.js](https://editorjs.io).

![](./img/prelaod.png)

## Features

- Uploading file from the device
- Preload image

**Note** This Tool requires server-side implementation for file uploading. See [backend response format](#server-format) for more details.

## Installation

### Manual downloading and connecting

1. Upload folder `dist` from repository
2. Add `dist/bundle.js` file to your page.

## Usage

Add a new Tool to the `tools` property of the Editor.js initial config.

```javascript
import Carousel from 'Carousel';

// or if you inject ImageTool via standalone script
const Carousel = window.Carousel;
 
var editor = EditorJS({
  ...

  tools: {
    ...
    carousel: {
                    class: Carousel,
                    config: {
                        endpoints: {
                            byFile: "URL_FETCH",
                        }
                    }
                },
  }

  ...
});
```
