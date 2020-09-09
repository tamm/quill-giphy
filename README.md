# quill-giphy

This is a POC of integration between Quill and the Giphy API.

Note: Giphy suggests using their SDK rather than API, and the included key is a rate limited beta key.

This is based on the [quill-emoji plugin](https://github.com/contentco/quill-emoji).

![Screenshot](/screenshot.png?raw=true "Screenshot")

## Prerequisites

[Quill.js](https://github.com/quilljs/quill), can also be `react-quill`;

## Getting set up

Install 
```
npm install https://github.com/tamm/quill-giphy.git -S
```
and import as 
```
import 'quill-giphy';
```

Then add to Quill config as

```
Editor.modules = {
  toolbar: {
    container: [
      ['giphy'],
    ],
    handlers: {
      'giphy': function() {}
    }
  },
  "giphy": true,
}
```

Visit https://developers.giphy.com/docs/api#quick-start-guide
to get an API key.

Then add your key to the global variable for config.
You can also change a couple of other settings:

```
const giphyOptions = {
  apiBase: 'https://api.giphy.com/v1',
  apiKey: 'YOUR-KEY-HERE', // https://developers.giphy.com/docs/api#quick-start-guide
  minimumCharactersToSearch: 3,
  debounceAPIRequestsMs: 300,
}
```

## License

Quill and `quill-emoji` are MIT Licensed, thus this plugin is too.