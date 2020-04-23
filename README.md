# Phone Preview
Draggable live phone preview modal for [Tinymce WYSIWYG editor]("https://www.tiny.cloud/").

![demo](phone-preview-demo.gif)

To use this plugin copy the folder "phonepreview" and paste it into tinymce "plugins" folder in its source directory.
Here's the path for tinymce_5.2.0 self-hosted production release -> tinymce_5.2.0/tinymce/js/tinymce/plugins

Download any of tinymce self-hosted releases [here](https://www.tiny.cloud/get-tiny/self-hosted/).

## Tutorial
### Initializing
In order to have it in your editor, after including _phonepreview_ folder in your tinymce plugins directory, you must tell tinymce to inlcude the plugin as well as its toolbar toggle button as demonstrated bellow...
```javascript
tinymce.init({
    selector: "#target-element", // change this value according to your HTML target element selector
    toolbar: ["phonepreview"],
    plugins: ["phonepreview"],
});
```
### Extending external CSS into PhonePreview
If you have already applied external CSS into tinymce editor by setting the [__content_css__](https://www.tiny.cloud/docs/configure/content-appearance/#content_css) property when initializing it, by default, the same CSS will be applied to PhonePreview. If for some reason you want to apply a different styling to PhonePreview, set the following property with the source path of the CSS file you want it to use.

```javascript
    tinymce.init({
        selector: "#target-element", // change this value according to your HTML target element selector
        toolbar: ["phonepreview"],
        plugins: ["phonepreview"],
        phone_preview_css: "assets/css/phone-preview.css"; // resolved to http://domain.mine/assets/css/phone-preview.css
    });
```
## Functionality
You can only open PhonePreview by clicking on its toggle button; however, you can close it by either clicking on its toggle button again or simply hitting the Escape key button (ESC).

PhonePreview is draggable. Just click on its frame, hold it and drag it around. You will soon notice that you cannot drag it off the screen - that's due to the fact that dragging PhonePreview has been limited to viewport size. 

Closing PhonePreview does not reset it to its initial position. As soon as you reopen it, it will be exactly where you left it. Reloading the whole page, however, will do just that.

Editing Tinymce content will automatically update PhonePreview content making it a LIVE phone preview component.

## Applying layout template into PhonePreview
Coming soon...

## Author
* [Melqui Brito](https://github.com/melquibrito)

## License
This project is licensed under the __MIT License__ - see the [LICENSE](LICENSE.md) file for more details.
