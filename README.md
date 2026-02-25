_Archived 20th Feb - the data needs to be deposited in Zenodo_

# metadata

This repository holds metadata about data and digital assets used in the MAMBO Habitat shrub project. The data is all made available under a Creative Commons Attribution 4.0 license.

## Data in cloud storage

We provide a world-readable s3 bucket kindly hosted by JASMIN / SFTC for the duration of the project.

You can connect to this bucket using standard open source geospatial libraries and tools, from the commandline, or view the data on the web.

Please see the [workshops](https://github.com/MAMBO-Habitat/workshops/) repository for example notebooks that show this data being used, which can be run locally or within Google Colab.

* [index.txt](index.txt) - all the URLs for direct access to data via HTTPS

### s3 bucket connection details


Example configuration to set up your python environment for access to the bucket.
```
import os
os.environ['AWS_S3_ENDPOINT'] = 'ukcehdrs-o.s3-ext.jc.rl.ac.uk'
os.environ['AWS_ENDPOINT_URL'] = 'https://ukcehdrs-o.s3-ext.jc.rl.ac.uk'
os.environ['AWS_VIRTUAL_HOSTING']="False"
os.environ['AWS_HTTPS']="True"
os.environ['AWS_NO_SIGN_REQUEST'] = "True"
os.environ['AWS_SECRET_ACCESS_KEY'] = ""

s3 = s3fs.S3FileSystem(anon=True)
```

## In progress - catalogue

STAC catalogue in JSON format in this repository describing the data collection that's currently in a world-readable s3 bucket provided by JASMIN, the STFC-supported research datacentre for environmental science.

Possibly some metadata about the repositories and any linked projects and teams.

## Setup

```
uv sync
py.test
```
