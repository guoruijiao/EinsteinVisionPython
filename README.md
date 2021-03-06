[![codecov](https://codecov.io/gh/feliperyan/EinsteinVisionPython/branch/master/graph/badge.svg)](https://codecov.io/gh/feliperyan/EinsteinVisionPython)
[![travis-ci](https://travis-ci.org/feliperyan/EinsteinVisionPython.svg?branch=master)](https://travis-ci.org/feliperyan/EinsteinVisionPython)
# EinsteinVisionPython

### Very much a work in progress Python Wrapper for the [Einstein Predictive Vision API service](https://devcenter.heroku.com/articles/einstein-vision)

### Installation:

```bash
pip install EinsteinVision
```

### Usage Example (also see examples folder for multi-threaded example)

```python
from EinsteinVision.EinsteinVision import EinsteinVisionService

genius = EinsteinVisionService(email='<your_username@email.com>', pem_file='<pem file>')
genius.get_token()

r = genius.get_datasets_info()

# requests object
r.json()
```

2017-08-16 At the moment you can use this to:
1. Read a .pem file (remember you can copy-paste your primary key into a file and name it .pem)
2. Generate an Auth Token
3. Send an image URL and a modelId (GeneralImageClassifier if you want) and get a prediction
4. Upload an image file as base64 for prediction
5. Create a dataset from an accessible zip url
6. Train a model given a dataset id
7. Check on status of training
