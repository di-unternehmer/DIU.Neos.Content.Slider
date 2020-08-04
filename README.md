
# DIU Neos Content Slider

This package adds slider functionality to your site. We use Swiper for this package.
                                                     
https://swiperjs.com/


## Constraints in your site package (example)

To restrict the content elements which should be slideable you should overwrite the constraints in you site package like this example.

```
'DIU.Neos.Content.Slider:Embed':
  childNodes:
    slides:
      constraints:
        nodeTypes:
          '*': false
          'DIU.Grid:Content.Structure.Section': true
          'DIU.Neos.Content.Picture:Picture': true

```

## Required resources

This package autoincludes the required js and css into Neos.Neos:Page but you can prevent them to load und include it into your frontend build process by overwriting the fusion code in your site package.

```
prototype(Neos.Neos:Page) {
    sliderStyles = null
    sliderScript = null
}
```

You will need to include these files into your frontend build:

```
/Public/JavaScript/swiper-bundle.min.js
/Public/Styles/swiper-bundle.min.css
/Private/Fusion/Embed/Embed.js
/Private/Fusion/Embed/Embed.css 
```
