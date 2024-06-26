
==============
sourceplus-sdk
==============


    Search, curate, and enrich collections for AI training.


`Source.Plus <https://source.plus>`_ is a platform that enables users to search, curate, and enrich collections for AI training. This SDK provides a Python interface to the Source.Plus API.
At this time, this SDK only allows the downloading of image files exported from Source.Plus.


----------------
Before You Begin
----------------

First, you'll need your Download Key from Source.Plus. To get your Download Key, go to the `settings <https://source.plus/settings/keys>`_ page
in Source.Plus. Create a key if you don't already have one. This key is used to authenticate your requests to the Source.Plus API.

Set this key as an environment variable in your shell. You can do this by adding the following line to your shell profile (e.g. ~/.bashrc, ~/.zshrc, etc.)::

        export SOURCEPLUS_DOWNLOAD_KEY="your-download-key"

If you prefer to not make this change, then you can also provide your API Key during the download process.

------------
Installation
------------

First, you need to have pip installed on your system. If you don't have pip installed, you can install it by following the instructions `here <https://pip.pypa.io/en/stable/installing/>`_.

Next, you'll need to install the Source.Plus SDK. You can do this using pip::

        pip install sourceplus-sdk

-----
Usage
-----

Once you have installed the SDK, you can use it download images from a parquet file::

        sourceplus download_images -f /path/to/export.parquet -o /path/to/output/directory

This will download all the image URLs from the parquet file to the output directory. If you have not set the API Key environment variable,
the SDK will prompt you to enter your API Key.

----------------
Advanced Options
----------------

There are several options you can tune to adjust the behavior of the download process. You can see all the options by running::

        sourceplus download_images --help

This will show you all the available options and their descriptions.