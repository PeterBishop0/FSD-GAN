# The detailed network structures of FSD-GAN

Among the tables mentioned above, the input of the encoder network is a tensor of $3\times64\times64$ (i.e., RGB image with a height and width of 64 pixels, the same is true for the following), the input of the decoder network is a tensor of $512\times8\times8$, the input of the discriminator network is a tensor of $3\times64\times64$, and the input of the fingerprint generator is a tensor of $3\times64\times64$. 

$Conv$ stands for the convolutional layer, and $DeConv$ is the deconvolutional layer network. $k$, $p$, and $s$ are parameters of the convolution and deconvolutional layer, which represent the convolution or deconvolution kernel size, padding, and stride, respectively. $LReLU(LeakyReLU)$ and $Sigmoid$ are activation functions, and parameter settings of activation functions follow the work in \cite{zhu2017unpaired}. $Flatten$ is a flattening function used to transfer tensors in the network into a one-dimensional tensor. $Reshape$ is a reconstruction function used to change the dimension of a tensor without changing the total number of parameters. $PixelShuffle$ and its previous convolutional network constitute the upsampling function proposed in \cite{shi2016real}. $Linear$ is a fully connected layer, and $InstanceNorm2d$ is a widely used normalization layer.
