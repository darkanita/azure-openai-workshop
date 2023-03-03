# Running Demos

## Create Conda Environment
```bash
    conda create -n env-openai python=3.10
    conda activate env-openai
```

## Prepare Conda Environment
Use requirements.txt to install necessary packages
```bash
    pip install -r requirements.txt
```

## Setup Environmental Variable
Rename the file .env.template to .env and update the values for the following variables:
```bash
    ren .env.template .env
```

In the file .env you will need to setup the following environmental variables:

### Azure OpenAI Service

OPENAI_API_ENDPOINT=https://example-endpoint.openai.azure.com
OPENAI_API_KEY=example-key
OPENAI_API_VERSION=azure
OPENAI_API_TYPE=2022-12-01

### Azure Cognitive Search Service

This services is necessary for the demo query based search.

SEARCH_ENDPOINT=https://envopenai.search.windows.net
SEARCH_API_KEY=example-key
SEARCH_INDEX_NAME=example-index


### Models

First you must create the deployment for the models in OpenAI service.  Then you must setup the following environmental variables for the model deployment names.

TEXT_SEARCH_DOC_EMBEDDING_ENGINE=curie-search-doc-deployname
TEXT_SEARCH_QUERY_EMBEDDING_ENGINE=curie-query-doc-deployname
TEXT_DAVINCI_002=text-davinci-002-deployname
After creating Azure OPENAI service, setup 2 environmental variables for OPENAI API services,  

## Run Demo Code