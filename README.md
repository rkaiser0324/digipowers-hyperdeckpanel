# hyperdeckpanel

This project based on the [HyperDeckPanel](https://hyperdeckpanel.com/) project by [Jeff Amato](http://iamjeffamato.com/), with a few small bugs fixed. It is a PHP web application that communicates with the HyperDeck via a TCP socket on port 9993.

## Setup

1. Tested on PHP 7.3; add this to your `php.ini` to prevent warnings:
    ```ini
    xdebug.scream   = 0
    error_reporting = E_ERROR | E_USER_ERROR    
    ```
1. Update `config.json` as needed

You can then navigate to the URL for the panel.

## Sample TCP commands

```
open: tcp://1.2.3.4:9993
    
    remote: enable: true\r\n play\r\n

    remote: enable: true\r\n play\r\n

    configuration: file format: HFS+\r\n

    configuration: file format: exFAT\r\n
```

## Links

1. See the [jmew24/blackmagic-hyperdeck-ui](https://github.com/jmew24/blackmagic-hyperdeck-ui) Python project, which is a modified version of the [Blackmagic HyperDeck Developer SDK](https://www.blackmagicdesign.com/developer/product/hyperdeck).
