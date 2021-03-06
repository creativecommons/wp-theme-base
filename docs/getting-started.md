---
title: Getting started
date: 2020-09-08 12:05:54
slug: getting-started
description:
---

To get started you have to first install the CC WP Base Theme locally. 

## Requirements

  - [WordPress](https://wordpress.org/support/article/how-to-install-wordpress/)
  - [Composer](https://getcomposer.org/): Install composer globally by following the [documentation](https://getcomposer.org/doc/00-intro.md#globally) for your particular OS.

_For a step by step guide on how you can set up WordPress in your local environment checkout [How to set up a local development...](https://www.endpoint.com/blog/2019/08/07/set-up-local-development-environment-for-wordpress)_
## Installation Guide

1. Download the <a href="https://github.com/creativecommons/creativecommons-base/archive/master.zip">zip</a> package of the theme.
2. Unzip to your wp-content/themes directory.
3. Navigate to the wp-theme-base directory and run the command below on the terminal, to install all the necessary package dependencies:

```
composer install
```

One of the installed dependencies is [Queulat](https://github.com/felipelavinz/queulat). In-order to initialize Queulat in the project, follow the instructions provided in [feliperlavinz/queulat](https://github.com/felipelavinz/queulat#loading-queulat-as-mu-plugin). 

Alternatively, to initialize Queulat navigate to the mu-plugins directory. The mu-plugins directory is in the root of the wp-content folder. It’s automatically created when you install Queulat using composer. At the root of the mu-plugins directory create an index.php file. Then copy and paste the code below:

```php
<?php
/**
 * Plugin Name: Queulat Loader
 * Description: Load Queulat mu-plugin
 */
// Load Composer autoloader (ABSPATH it's the path to wp-load.php).
require_once ABSPATH . 'wp-content/themes/wp-theme-base/vendor/autoload.php';
// Load Queulat main file.
require_once __DIR__ .'/queulat/queulat.php';
```

4. Start your development server and activate the CC WP Base Theme in your local WordPress Dashboard.
