# RNN-attention-network
Here a simple implementation of RNN + attention neural network on IMDB movie reviews.

This is a implementation of NN(Neural Network) model Recurrent Neural network with an attentation layer, where for different RNN(Recurrent Neural Network) units i.e. Vannila, GRU(Gated Recurrent Unit) and LSTM(Long Short Term memory) are used For Experiment on IMDB movies review data set where dataset consist of 50,000 labeled reviews (selected for sentiment analysis, where The sentiment of reviews is binary i.e 0{negative} or 1{positive}), out of which 25,000 are for train  and 25,000 are for testing. There are various other parameters that has been used for experiment and explained in detail in **result.txt** file.

The model architecture is given below[Yang 2016]:

                               
       w(t) = t'th word in a given review                    [w(1), w(2), ...., w(t)]
                                                                         ↓
                                                    -----------------------------------------------
    X = [x(1),x(2),...,x(n)],   x(t) = We(w(t))    |            Word Embedding layer               |
                                                    -----------------------------------------------
                                                                          ↓
                                                    -----------------------------------------------
          h(t) = RNN(x(t), h(t-1))                 |                  RNN Layer                    |
                                                    -----------------------------------------------
                                                                          ↓
                                                    -----------------------------------------------
    u(t) = tanh(Ww.h(t) + bw)                      |                                               |
     α(t) = softmax(u(t).uw)                       |                Attention Layer                |
      s = sum(α(t) * h(t))                         |                                               |
                                                    -----------------------------------------------
                                                                          ↓
                                                                        [0,1]


The Results of the model with different RNN is given in **result.txt**.

[Yang 2016] Yang, Z., Yang, D., Dyer, C., He, X., Smola, A. and Hovy, E., 2016. Hierarchical attention networks for document classification. In Proceedings of the 2016 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (pp. 1480-1489).