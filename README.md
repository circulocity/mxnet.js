MXNetJS Deep Learning in Browser
================================
MXNetJS is the [dmlc/mxnet](https://github.com/dmlc/mxnet) Javascript package. MXNetJS brings state of art deep learning prediction API to the browser.
It is generated with [Emscripten](https://github.com/kripken/emscripten) and [Amalgamation](https://github.com/dmlc/mxnet/tree/master/amalgamation).
MXNetJS allows you to run prediction of state-of-art deep learning models in any computational graph, and brings fun of deep learning to client side.


Try it on Browser
-----------------

Online: [http://webdocs.cs.ualberta.ca/~bx3/mxnet/classify.html](http://webdocs.cs.ualberta.ca/~bx3/mxnet/classify.html)

Local:
```
python -m SimpleHTTPServer
```
Then open browser http://localhost:8000/classify.html

See [classify_image.js](classify_image.js) for how it works.

Speed
-----
On Microsoft Edge and Firefox, performance is at least 8 times better than Google Chrome. Usually an image takes 0.6 - 0.8 sec on FF/Edge, but 6 - 8 sec on Chrome. We assume it is optimization difference on ASM.js.


Use Your Own Model
------------------
MXNetJS can take any model trained with mxnet, use [tools/model2json.py](tools/model2json.py) to convert the model into json format and you are ready to go.

Library Code
------------
- [mxnet_predict.js](mxnet_predict.js) contains documented library code.
  - This is the code developer can call from
- libmxnet_predict.js is automatically generated by ```make rebuild``` and should not be modified by hand.


Contrbute to MXNetJS
--------------------
Contribution is more than welcomed!
