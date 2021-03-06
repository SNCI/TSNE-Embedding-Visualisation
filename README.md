# TSNE-Embedding-Visualisation
A Simple and easy to use way to Visualise Embeddings!

<p align="center">
  <img src="https://github.com/harveyslash/TSNE-Embedding-Visualisation/blob/master/demo.gif?raw=true" alt="Visualising Example"/>
</p>




### What this project is? 
This project is forked from [Tensorflow's Standalone Embedding Projector](https://github.com/tensorflow/embedding-projector-standalone).
It shows how a pretrained InceptionV3 model can be used on images and plotted in an interactive 3d map.


### Why this over the Standalone Projector? 
This project allows you to visualise any array of vectors with a light depency stack. It is designed to be decoupled form any library. Moreover , it uses a static file system, so you can publish your results without requiring a server. E.g. https://harveyslash.github.io/TSNE-Embedding-Visualisation/.

### Project Structure

    |-- data  <-- where to put raw data
    |-- Feature-extractor.ipynb <-- Demo of Embedding generation in a step by step fashion
    |-- index.html <-- The GUI of the Viewer (Do not touch, unless you know what youre doing)
    |-- LICENSE
    |-- main.py <-- Executable to generate embedding data from command line args
    |-- oss_data <-- required by the visualisation project
    |   |-- oss_demo_projector_config.json <-- all configuration files are stored here, this is modified by main.py automatically
    |   |-- sprites.png <-- sprites for the demo 
    |   `-- tensor.bytes <-- embeddings array for the demo
    `-- requirements.txt

### Installation and requirements
This project requires python3.6. You can install all dependencies using `pip install -r requirements.txt`

### Usage 
Usage: main.py [OPTIONS]

    Options:
      --data TEXT                 Data folder,has to end with /
      --name TEXT                 Name of visualisation
      --sprite_size INTEGER       Size of sprite
      --tensor_name TEXT          Name of Tensor file
      --sprite_name TEXT          Name of sprites file
      --model_input_size INTEGER  Size of inputs to model
      --help                      Show this message and exit.
  
  
