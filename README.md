# docfx-lightbox-plugin

A small repository containing a template for DocFx to add lightbox effect for all images.

## Fork from [roel4ez/docfx-lightbox-plugin](https://github.com/roel4ez/docfx-lightbox-plugin)

This is a fork from [roel4ez/docfx-lightbox-plugin](https://github.com/roel4ez/docfx-lightbox-plugin) to a NetStandard 2.0 project using the same sources.

I needed to upgrade it to fit the docfx version I use (2.40.8.0).

I also lightly modified the templates to add the `.modal-img` css class to the modal to add control to the styling of the modal.

For example, I added this to my CSS to make the modal fit the screen size :

``` css
.modal-img {
    width: 80%;
}
````

__Thanks to Roel for this nice plugin.__

## Featherlight

The first version of this template uses the jQuery [Featherlight](https://noelboss.github.io/featherlight/) plugin. Therefore, there is a dependencies on both of these libraries.  
It is using the default template from `docfx` as a base template.
jQuery and the featherlight libraries are loaded from the public CDN.

### Usage

To use this template, you need to add it to your repository in the `templates` folder, and add the following to your `docfx.json` file:

```json
   "template": [
      "default",
      "templates/lightbox-featherlight"
    ]
```

### Demo

A sample can be found in the `demo` folder. It uses a relative path to the `templates` folder.

## Bootstrap modal

The second version of this plugin uses the Bootstrap Modal window, and is created by implementing `IPostProcessor`.  
