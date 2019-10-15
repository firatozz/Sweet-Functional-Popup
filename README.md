# Sweet Functional Popup
<p align="left">
  <img src="https://i.imgyukle.com/2019/10/15/ENwm8j.png" width="200px" height="200px">
</p>

# New Features!
 - Customizable via CSS.
 - Customizable via HTML.
 - Cookie support with optional expiry date.
 - Pageviews Counter (Show after the number of pageviews)
 - Set a timed delay before the script starts tracking show notification box.
 - Auto Close with Timer
 - Page scroll control
 - LightBox or Exit Intent Usage
 - 4 different animations
 - Show once per session Option
 - Re-direct and new tab management

# Usage

Simply include the script and call its init function with any options you choose. 

```js
<script type="text/javascript" src="sweetFunctionalPopup.min.js"></script>

<script type="text/javascript">
   var popUp = new sweetFunctionalPopup();
    popUp.setOptions({
        // options..
    });
</script>
```

### Customize style with CSS
You can change CSS attirbutes on init function.
```js
<script type="text/javascript" src="sweetFunctionalPopup.min.js"></script>

<script type="text/javascript">
    var popUp = new sweetFunctionalPopup();
    popUp.setOptions({
        .
        .
        css: ".ltImg{border-radius:10px;}",
        .
        .
    });
</script>
```

# Options

All options must be added to the init function as an object.

| Option | Type | Default | Description 
| ------ | ------ | ------ | ------ |
| autoClose | Integer | 0 | The popup will be closed according to this timing value. (Exp: 1 *1000 ms)
| animation | String | fade | The animation of the notification box. It have 3 different animations. "blur", "fade", "bubble", "classic". You have to write the value you want to use as it is here.
| width | Integer | 300 | The width of the notification box.
| height | Integer | 300 | The height of the notification box.
| imageUrl | String | icon-image | The image you want to show
| targetUrl | String | # | re-direction link
| targetOpenNewTab | boolean | true | This would be added "_blank" or "_self" after click.
| delay | Integer | 1 | The time, in seconds, until the notification box activates.
| canScroll | Boolean | false | Scroll control of the back page after the popup is displayed.
| customHTML | String | null | The custom HTML codes for the popup.
| css | String | null | The CSS styles for the notification box. CSS can be added through this function or on the page itself.
| showAsExitIntent | Boolean | false | Popup works as exit intent.
| cookieExp | Integer | 7 | The number of days to set the cookie for. A cookie is used to track if the notification box has already been shown to a specific visitor. If the notification box has been shown, it will not show again until the cookie expires. A value of 0 will always show the notification box.
| showOncePerSession | Boolean | false | If true, the notification box will only show once per browser session. If false and cookieExp is set to 0, the notification box will show multiple times in a single browser session.
| showCountPageviews | Integer | 0 | The pop-up will be displayed after the number of page views given. If it is 0, it will always be running.

### Animations Value Types

| Option | Default | Value Names |  
| ------ | ------ | ------ 
| animation | fade | fade, blur, bubble, classic

CAUTION !: The values are case sensivity, so the values must be entered correctly.



# Example
```html
<!DOCTYPE html>
<html>
<head>
    <script type="text/javascript" src="liteNotificationBox.min.js"></script>
</head>
<body></body>
<script type="text/javascript">
 liteNotificationBox.init({
        position: "bottomLeft",
        animation: "bubble",
        width: 200,
        height: 200,
        imageUrl: "https://blog.addthiscdn.com/wp-content/uploads/2015/11/JS-360454.png",
        targetUrl: "github.com",
        targetOpenNewTab: true,
        delay: 5,
        css: ".ltImg{border-radius:10px;}",
        cookieExp: 7,
        showOncePerSession: false,
    });
</script>
</html>
```

License
----

MIT license - https://opensource.org/licenses/MIT

**Free Software, Hell Yeah!**
