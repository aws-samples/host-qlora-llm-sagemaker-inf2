# Host a QLoRA finetuned LLM using inferentia2 in Amazon SageMaker

## Overview
This repository demonstrates how you could finetune a llama2 model using PEFT technique, such as QLoRA, and convert the quantized model to the AWS neuron compatible format. 
The converted neuron model is deployed to an inf2 instance using a DJL serving container in SageMaker environment..


## Getting Started
This repo contains 2 notebooks: 

1. [finetune llama2](llama2-7b-finetune-qlora.ipynb) should be run first to create a finetuned model with LoRA adapter weights. 

2. [Deploy the QLoRA model in SageMaker for inference](deploy_finetuned_llama_2.ipynb) should be run after the finetuned model artifact has been uploaded to an S3 bucket.

The first notebook has been tested in a ml.g5.2xlarge instance in SageMaker Studio using a Pytorch 2.0 GPU Optimized kernel.

The second notebook has been tested in a SageMaker Studio ml.t3.medium notebook instance with Data Science 3.0 and Python kernel.
