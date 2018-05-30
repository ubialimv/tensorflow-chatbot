# Tensorflow Chatbot

Dependencies
============
* numpy
* scipy 
* six
* tensorflow (https://www.tensorflow.org/versions/r1.8/get_started/os_setup.html)

Use tensorflow out of an Anacoda environment. Follow the steps to install tensorflow on the site above, consider using it with GPU, so install CUDA and cuDNN.

Use pip to install any missing dependencies

Usage
===========

Training
--------------------

0. Create directories
    ```
    working_dir
    data
    ```

1. Download the [Cornell Movie Dialogue dataset](https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html) and place the unzipped content in the `data/` directory.

2. Prepare data for training, in the `data/` directory, run the `prepare_data.py` script
    ```
    python prepare_data.py
    ```

3. To train the bot, edit the `seq2seq.ini` file so that mode is set to train like so

`mode = train`

4. Start training, by running the code like so:

    ``python execute.py``

> There is no mechanism to stop training, you will need to 'ctrl-c' to stop training after a period of time.


Test
-------------

1. To test the bot during or after training, edit the `seq2seq.ini` file so that mode is set to test like so

    `mode = test`

2. To test run the code like so:

    ```
    python execute.py

    >> Mode : test

    Reading model parameters from working_dir/seq2seq.ckpt-00000
    >    
    ```

3. Type something to test
    - Are you a smart chatbot?
