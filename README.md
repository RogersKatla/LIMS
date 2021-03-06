# LABORATORY INFORMATION MANAGEMENT SYSTEM FOR [DOLIBARR ERP CRM](https://www.dolibarr.org)

## Features v0.1.0

Manage your samples and generate test reports following ISO 17025:2017: 
* Manage Test Methods, where each method has
  * A linked product or service
  * A unit, e.g. mS/cm
  * Accuracy
  * Measurement Range
  * Resolution of reading
* Manage Limit Sets, with each entry/line
  * Linked to one method
  * Minimum and Maximum, where one value may be NULL
* Manage Samples, where each sample has
  * A linked to a customer
  * Details on the sample, such as sampling place and time, sampling person, volume, etc.
  * Muliple tests, where each test is linked to one method; each test is linked to the responsible person
  * Nonconformities
  * A limit set applied to the sample results
* Test Report
  * Sample details
  * Results with indication if result is out of the limit range or out of the method's measurement range
  * Names of person(s) responsible and manager who authorized the sample.

<!--
![Screenshot lims](img/screenshot_lims.png?raw=true "LIMS"){imgmd}
-->

Other modules are available on [Dolistore.com](https://www.dolistore.com>).

## Translations

Translations can be defined manually by editing files into directories *langs*. Currently available language files: English.

<!--
This module contains also a sample configuration for Transifex, under the hidden directory [.tx](.tx), so it is possible to manage translation using this service.

For more informations, see the [translator's documentation](https://wiki.dolibarr.org/index.php/Translator_documentation).

There is a [Transifex project](https://transifex.com/projects/p/dolibarr-module-template) for this module.
-->


## Installation

### From the ZIP file and GUI interface

* Download a release package from https://github.com/NDUWRDC/LIMS/releases
* Log into Dolibarr as admininistrator and browse to ```Home - Setup - Modules/Applications```
  * Select tab ```Deploy/install external app/module```
  * Select the zip-file (release package) and click SEND

Note: If this screen tell you there is no custom directory, check your setup is correct:

- In your Dolibarr installation directory, edit the ```htdocs/conf/conf.php``` file and check that following lines are not commented:

    ```php
    //$dolibarr_main_url_root_alt ...
    //$dolibarr_main_document_root_alt ...
    ```

- Uncomment them if necessary (delete the leading ```//```) and assign a sensible value according to your Dolibarr installation

    For example :

    - UNIX:
        ```php
        $dolibarr_main_url_root_alt = '/custom';
        $dolibarr_main_document_root_alt = '/var/www/Dolibarr/htdocs/custom';
        ```

    - Windows:
        ```php
        $dolibarr_main_url_root_alt = '/custom';
        $dolibarr_main_document_root_alt = 'C:/My Web Sites/Dolibarr/htdocs/custom';
        ```

### From a GIT repository

- Clone the repository in ```$dolibarr_main_document_root_alt/lims```

```sh
cd ....../custom
git clone https://github.com/NDUWRDC/LIMS.git lims 
```

### <a name="final_steps"></a>Final steps

From your browser:

  - Log into Dolibarr as administrator
  - Go to ```Home - Setup - Modules/Applications```
  - You should now be able to find and enable the module LIMS

## Licenses

### Main code

GPLv3 or (at your option) any later version. See file COPYING for more information.

### Documentation

All texts and readmes are licensed under GFDL.
