
```
var express = require('express');
var app = express();

app.use('/js', express.static(__dirname + '/public/js'));
app.use('/css', express.static(__dirname + '/public/css'));
app.use('/assets', express.static(__dirname + '/public/assets'));
app.use('/views', express.static(__dirname + '/public/views'));

app.all('/*', function(req, res, next) {
    res.sendFile('/public/index.html', { root: __dirname });
});

app.listen(3000);
```

# Angular-Base
A simple Angular/NodeJS base to kickstart apps that allows for controllers, views, services, and single page applications with just a git clone.


## Built With
* Angular - for a Single Page Application feel that's more seamless for users
* JavaScript - for building out controllers, index.js file, etc


##Installation instructions:
* Git clone
* NPM Install 
* Create DB side of things (optional)
* Change App/Ctrl/Services names in public/js

## Future Goals
* include simple MongoDB and SQL library startups

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

