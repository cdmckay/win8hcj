# Accessing and Calling Files

## Namespace

````
# Project Package file access protocol/schema
ms-appx://

# Project root
ms-appx:///
## Note the three '/'. The third '/' references the package root.  The app will assume the root of the app package.

# Example
ms-appx:///default.html
## Refers to the default.html file that is at the root of the app package.
````

## Accessing Local Project Files

### Via HTML

````html
<script src="images/logo.png">
````

### Programatically

````javascript
var uri = new Windows.Foundation.Uri('ms-appx:///images/logo.png');
var file = Windows.Storage.StorageFile.getFileFromApplicationUriAsync(uri);
````

## Accessing Remote Files

For images on the web you can retrieve them as you normally would when writing HTML.

````html
<img src="http://www.example.com/images/logo.png" alt="Logo" />
````