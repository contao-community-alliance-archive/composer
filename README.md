Composer
========

Mini module which loads the composer autoloader, creates initial composer.json

### Installation

##### Checkout repository

Checkout this repository and link it to system/modules (initial)

```
cd /path/to/my/project/documentroot
git clone git@github.com:ContaoCommunityAlliance/Composer.git composer/vendor/contao-community-alliance/composer
cd system/modules
ln -s ../../composer/vendor/contao-community-alliance/composer/src/system/modules/_composer .
cd ../..
```

##### Contao page request

Do a normal page request, this will prepare the folder structure and the default composer.json

##### Download composer

Download composer as explained here: http://getcomposer.org/doc/00-intro.md#downloading-the-composer-executable

```
cd ./composer
curl -sS https://getcomposer.org/installer | php
```

##### Add some vendors

Add some vendors to the composer.json as explained here: http://getcomposer.org/doc/04-schema.md

```json
{
    "require": {
        "contao-community-alliance/composer-installer": "dev-master@dev",
        "contao-community-alliance/composer": "dev-master@dev"
    }
}
```

##### Install the vendors

Tell composer to download the configured vendors

```
php composer.phar install
```


### Requirements
* php 5.3.4 or higher
* php command line and the access to use it
* contao 2.11.*