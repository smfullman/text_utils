# Text Processing Notebooks

A smattering of notebooks.  Useful for jump starting text projects.

### Notebooks

* 00_word_embeddings: Create word embeddings using word2vec
* 01_topic_model: Create a topic model 
* 02_baseline_models: Vectorize text and classify with linear models 
* 03_sequential_models: Classify with RNNs


### Dockerfile

A dockerfile that can be used to create an image which runs all notebooks.  Uses GPU implementations of tensorflow and keras.  Requires nvidia-docker: https://github.com/nvidia/nvidia-docker/wiki/Installation-(version-2.0)

To build:
<pre>
docker build -t image_name .
</pre>

To run:
<pre>
NV_GPU=1 nvidia-docker run -it -p 9999:9999 -v /your/notebook/folder:/home image_name /bin/bash -c "/opt/conda/bin/jupyter notebook --notebook-dir=/home --ip=* --port=9999 --no-browser --allow-root"
</pre>
