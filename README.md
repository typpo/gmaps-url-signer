# gmaps-url-signer

This is a node.js URL signer for Google Maps API Web Services.  It simply packages Google's documentation and example code provided [here](https://github.com/googlemaps/url-signing/blob/gh-pages/urlSigner.js) into a Node module.

URL signing is used in the Static Maps, Directions, Geocode API, and more.

This library is available as an [npm package](https://www.npmjs.com/package/gmaps-url-signer).  To install, run:

    npm install gmaps-url-signer

Here's an example of how you can use this library:

    const urlSigner = require('gmaps-url-signer');
    
    const key = 'my_google_api_key';
    const secret = 'my_static_maps_secret';
    const domain = 'http://maps.googleapis.com';

    // Path to your static map
    let path = '/maps/api/staticmap?zoom=2&scale=1&size=350x250&maptype=terrain&format=png&visual_refresh=true';
    path += `&key=${key}`;

    console.log('Full signed URL:');
    console.log(domain + urlSigner.sign(path, secret));

You can see it in action on [dinosaurpictures.org](http://dinosaurpictures.org/Tyrannosaurus-pictures) (check out those static maps!)
