# social media post image finder with Clip model
- Developed and implemented a CLIP model from scratch without using the already built pretrained model from openai. 
Implement a prompt caption(text) to retrieve images similar to the text

CLIP is a multi-modal vision and language model. It can be used for image-text similarity and for zero-shot image classification. CLIP uses a ViT like transformer to get visual features and a causal language model to get the text features 
OpenAI has open-sourced some of the code relating to CLIP model so we developed the model with PyTorch 
- Dataset
The dataset was sourced for kaggle downloaded the data from the Kaggle api call environment.
We use Flickr 8k dataset containing the images and some text describing them
# Process
- Config class
its a class defined in the beginning of the notebook to keep all the hyperparameters.

- Utils class 
Contains functions that prepares the dataset
- Dataset  processing 
we need to encode both images and their describing texts. So, the dataset needs to return both images and texts.
- Image Encoder
encodes each image to a fixed size vector with the size of the model's output channels (in case of ResNet50 the vector size will be 2048). 
- Text Encoder
use DistilBERT as the text encoder


- CLIP model
Developed a CLIP model class containing functions for the image encoding, text encoding and projection head

- Training
Created a Training, evaluation and dataloader function loop and loading it in batch processing 
- Results
Write a function to find similar image pair for a text query and it give an output of 9 images similar to the text.
