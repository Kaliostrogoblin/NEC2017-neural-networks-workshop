# NEC2017-neural-networks-workshop

This repository contains files that was showed on the NEC-2017 symposium as presentation of keras functionality to building deep neural networks.

- *Workshop.ipynb* is an ipython notebook, that includes main code examples
- *data* directory stores all trained models of neural networks from workshop. Feel free to download them and test

All files in *data* with .json format are keras graphs, .h5 files are weights of the models, specyfied by graphs with the same names as weights files.

To load neural networks (RNN, for example) from files one can use this snippet of python code:
```python

from keras.models import model_from_json

with open('data/RNN.json', 'r') as f:
    RNN = model_from_json(f.read())
RNN.load_weights('data/RNN.h5')
```  