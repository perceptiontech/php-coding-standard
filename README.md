# Perception PHP coding standard

This standard follows the (Symfony standards)[https://symfony.com/doc/current/contributing/code/standards.html] with
with the following exceptions:

- It does not require the license on top of every file.
- It allows to have multiline function arguments.

## Installation steps

1. Install PHP code sniffer: https://github.com/squizlabs/PHP_CodeSniffer#installation
2. Require package globally using composer:

    ```bash
    $ composer global require "perceptiontech/php-coding-standard"
    ```

3. Add the coding standard to the PHP_CodeSniffer install path (under MacOS and Linux):

    ```bash
    $ phpcs --config-set installed_paths ~/.composer/vendor/perceptiontech/php-coding-standard
    ```
    
    Be aware that, if you already have installed paths, they will be lost. If so, you will have to execute:
    
    ```bash
    $ phpcs --config-set installed_paths ~/.composer/vendor/perceptiontech/php-coding-standard,/path/to/already/insatlled/standard/
    ```

4. Check the installed standards for "Perception":

    ```bash
    $ phpcs -i
    ```

## PHPStorm configuration

### Code_Sniffer configuration

1. Go to quality tools, unfold the Code Sniffer option and toggle the configuration by clicking on `...`:

    ![PHPStorm CodeSniffer configuration](/img/img-01.png)

2. Set the path to your local PHPCode_Sniffer binary and validate it:

    ![PHPStorm CodeSniffer binary](/img/img-02.png)

### Ruleset configuration

1. Go to Editor > Inspections > PHP > Quality tools > PHP Code Sniffer validation

    ![PHPStorm CodeSniffer insepctions](/img/img-03.png)

2. Enable the configuration, refresh the "Coding standard" and select "Perception". Configuration should be as it follows:

    ![PHPStorm CodeSniffer insepctions](/img/img-04.png)
    
    (NOTE: set the severity as "warning". Otherwise, it is difficult to spot the errors within the editor)

3. After this configuration, PHPStorm should inform you whenever a piece of code is not correct according to the rules:

    ![PHPStorm CodeSniffer insepctions](/img/img-05.png)