# lagllama_demo
This demo includes a container for runing Lag Llama in Snowflake Container Services. The container includes the Lag Llama and the GluonTS packages necessary for getting predictions. A sample notebook is included, but you will have to connect to your own time series data sources (a sample dataset is provided in the repo). dd

1. Build the Docker image
   docker build --rm --platform linux/amd64 -t lagllama .
                             
3. Tag and push it to Snowpark container services image repo
   docker tag lagllama
   Based on the location of your image folder:
   sfsenorthamerica-polaris2.registry.snowflakecomputing.com/mistral_vllm_db/public/images/lagllama
   docker push sfsenorthamerica-polaris2.registry.snowflakecomputing.com/mistral_vllm_db/public/images/lagllama
   
3. Push the lagllama_spec.yaml @yamls stage to your stage. Make sure the spec file is set to your environment.
   
## Time Series Modeling

1. Start in jupyter server
2. Navigate to ll_github folder
3. Open the LagLlama.ipynb folder
4. To run the demo model, upload the data, timedata.csv which is in the github here
5. The notebook will show you the data, run predictions, plot the predictions, and provide evaluation statistics 



