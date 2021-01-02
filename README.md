# MLWithPython


#How to integrate python with rstudio ?

https://cran.r-project.org/web/packages/reticulate/vignettes/python_packages.html

https://support.rstudio.com/hc/en-us/articles/360023654474-Installing-and-Configuring-Python-with-RStudio

https://linuxize.com/post/how-to-install-pip-on-ubuntu-18.04/




python environments in 

Matplotlib is building the font cache; this may take a moment.
Python 3.6.11 (/home/sravan/.local/share/r-miniconda/envs/r-reticulate/bin/python)


there is problem in configuring with python in Rstudio 
finding the python file paths
reticulate problems
project directory file paths

Part 7 : Natural Language Processing for PyTorch and TensorFlow 2.0 -Transformers in NLP
Transformers provides thousands of pretrained models to perform tasks on texts such as classification, information extraction, question answering,       summarization, translation, text generation, etc in 100+ languages. Its aim is to make cutting-edge NLP easier to use for everyone.


We use pipeline AI group. Quickly use a pipeline to classify positive versus negative texts.
    
    from transformers import pipeline
#Allocate a pipeline for sentiment-analysis

    classifier = pipeline('sentiment-analysis')
    classifier('We are very happy to include pipeline into the transformers repository.')
    [{'label': 'POSITIVE', 'score': 0.9978193640708923}]
    
       from transformers import pipeline

#Allocate a pipleline for question-answering

    question_answerer = pipeline('question-answering')
    question_answerer({
     'question': 'What is the name of the repository ?',
     'context': 'Pipeline have been included in the huggingface/transformers repository'
    })
    {'score': 0.5135612454720828, 'start': 35, 'end': 59, 'answer': 'huggingface/transformers'}

To download and use any of the pretrained models on your given task, you just need to use those three lines of codes 
(PyTorch version):

    from transformers import AutoTokenizer, AutoModel
    tokenizer = AutoTokenizer.from_pretrained("bert-base-uncased")
    model = AutoModel.from_pretrained("bert-base-uncased")
    inputs = tokenizer("Hello world!", return_tensors="pt")
    outputs = model(**inputs)

or for TensorFlow:

    from transformers import AutoTokenizer, TFAutoModel
    tokenizer = AutoTokenizer.from_pretrained("bert-base-uncased")
    model = TFAutoModel.from_pretrained("bert-base-uncased")
    inputs = tokenizer("Hello world!", return_tensors="tf")
    outputs = model(**inputs)

for more details please refer https://github.com/huggingface/transformers

Part 11. Federated learning PaddlePaddleFL deployment in Docker and kubernetes 
        
        PaddlePaddleFL deployment in Docker and kubernetes
        PaddlePaddleFL deployment in cloud environement
        PaddlePaddleFL deployment in local environement like in Raspberry Pi4.


How to run PaddleFL in Docker.
  
    #Pull and run the docker
    docker pull paddlepaddle/paddlefl:latest
    docker run --name <docker_name> --net=host -it -v $PWD:/paddle <image id> /bin/bash

    #Install paddle_fl
    pip install paddle_fl

#Easy deployement with kubernetes
#Data parallel

    kubectl apply -f ./python/paddle_fl/paddle_fl/examples/k8s_deployment/master.yaml

To resolve erros while installing. please run the below commands.

1. install upgrading version of pip by running below command
  
        /usr/local/bin/python3.8 -m pip install --upgrade pip

#required below version to be installed.
    
    paddlepaddle 1.8.5 requires opencv-python<=4.2.0.32
    paddlepaddle-gpu 1.8.5.post107 requires opencv-python<=4.2.0.32,

2. in order to install, please run the below command.
      
        pip install opencv-python==4.2.0.32

3.please re-run the below command, now you will see no erros.
 
        #Install paddle_fl
         pip install paddle_fl

Optimized models 

Mobilnet : 
DistilBERT :
Tensorflow Lite :
Raspberry Pi4 :

