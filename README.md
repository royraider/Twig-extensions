Plemi Twig extensions
=====================

# Base64 encoding for images

Basic Twig function to allow base64 images encoding following latest RFC.


# Usage in the real world

First of all, add this to your composer.json.

```json
{
    "require": {
        "plemi/twig-extensions": "dev-master"
    }
}
```

## Symfony2

```xml
<service id="plemi.twig.base64_extension" class="Plemi\Twig\Extensions\Base64Extension" public="false">
    <tag name="twig.extension" />
</service>
```

## Silex

```php
<?php

// After registering Twig Silex Provider
$app['twig']->addExtension(new \Plemi\Twig\Extensions\Base64Extension());
```

Then in your twig templates, just call the function with the file path as an argument.

```
{{ image64('/images/logo.jpg') }}
```