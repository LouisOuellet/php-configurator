![GitHub repo logo](/dist/img/logo.png)

# phpConfigurator
![License](https://img.shields.io/github/license/LouisOuellet/php-configurator?style=for-the-badge)
![GitHub repo size](https://img.shields.io/github/repo-size/LouisOuellet/php-configurator?style=for-the-badge&logo=github)
![GitHub top language](https://img.shields.io/github/languages/top/LouisOuellet/php-configurator?style=for-the-badge)
![Version](https://img.shields.io/github/v/release/LouisOuellet/php-configurator?label=Version&style=for-the-badge)

## Description
The phpConfigurator class is a PHP implementation for managing configuration files in a simple JSON-based format. It provides an interface for adding, deleting, getting, and setting configurations in these files.

## Features
  - **Simple configuration management**: The class provides a straightforward way to manage configurations for an application. It uses JSON files to store configurations, making it easy to read and write settings using native PHP functions.
  - **Reusability**: The class can be easily integrated into any PHP project that requires configuration management. It's not tied to a specific framework or project structure, so developers can reuse the class across multiple projects.
  - **Modularity**: The class allows developers to organize configurations into separate files, promoting modularity and making it easier to manage application settings. Each file can be dedicated to a specific part of the application, reducing the risk of conflicts between settings.
  - **Flexibility**: The phpConfigurator class provides a simple API to add, delete, get, and set configurations. Developers can extend or modify the class to add more advanced features or adapt it to their specific needs.

## Why you might need it?
In summary, the phpConfigurator class offers a simple and maintainable way to manage configurations in a PHP application. It can be easily integrated into any project and promotes modularity, reusability, and flexibility. However, it's important to note that this class does not provide any built-in encryption or protection for sensitive data, so it may not be suitable for storing sensitive information without additional security measures.

## Can I use this?
Sure!

## License
This software is distributed under the [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html) license. Please read [LICENSE](LICENSE) for information on the software availability and distribution.

## Requirements
* PHP >= 7.3

## Security
Please disclose any vulnerabilities found responsibly – report security issues to the maintainers privately.

## Installation
Using Composer:
```sh
composer require laswitchtech/php-configurator
```

## How do I use it?
### Usage
#### Initiate phpConfigurator
To use `phpConfigurator`, simply include the phpConfigurator.php file and create a new instance of the `phpConfigurator` class. By default, it will create a log file named "default.log" in the same directory as the phpConfigurator.php file.

```php

//Import phpConfigurator class into the global namespace
//These must be at the top of your script, not inside a function
use LaswitchTech\phpConfigurator\phpConfigurator;

//Load Composer's autoloader
require 'vendor/autoload.php';

//Initiate phpConfigurator
$phpConfigurator = new phpConfigurator();
```

#### Add a configuration file using the `add()` method
```php
$phpConfigurator->add('my_config');
```
If the configuration file is located in a custom directory, you can pass the path as the second argument:

```php
$phpConfigurator->add('my_config', '/custom/path/to/my_config.cfg');
```

#### Retrieve a setting from the configuration file using the `get()` method:
```php
$Value = $phpConfigurator->get('my_config', 'setting_key');
```

#### Set a new value for a setting in the configuration file using the `set()` method:
```php
$phpConfigurator->set('my_config', 'setting_key', 'new_value');
```

#### Delete a configuration file using the `delete()` method:
```php
$phpConfigurator->delete('my_config');
```
