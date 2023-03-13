# Image Classification using AWS SageMaker

Use AWS Sagemaker to train a pretrained model that can perform image classification by using the Sagemaker profiling, debugger, hyperparameter tuning and other good ML engineering practices. This can be done on either the provided dog breed classication data set or one of your choice.

## Project Set Up and Installation
Enter AWS through the gateway in the course and open SageMaker Studio. 
Download the starter files.
Download/Make the dataset available. 

## Dataset
The provided dataset is the dogbreed classification dataset which can be found in the classroom.
The project is designed to be dataset independent so if there is a dataset that is more interesting or relevant to your work, you are welcome to use it to complete the project.

### Access
Upload the data to an S3 bucket through the AWS Gateway so that SageMaker has access to the data. 

## Hyperparameter Tuning
What kind of model did you choose for this experiment and why? Give an overview of the types of parameters and their ranges used for the hyperparameter search

Remember that your README should:
- Include a screenshot of completed training jobs 

in the file 

- Logs metrics during the training process
- Tune at least two hyperparameters
- Retrieve the best best hyperparameters from all your training jobs

## Debugging and Profiling
**TODO**: Give an overview of how you performed model debugging and profiling in Sagemaker

1- downloaded smdebug in sagemaker
2- set up the dependencies
3-profiler configurations and debugger configurations
4-set up  estimator and fit it to  dog images data.

### Results
**TODO**: What are the results/insights did you get by profiling/debugging your model?
it toke 25m to finsh 
**TODO** Remember to provide the profiler html/pdf file in your submission.
done

## Model Deployment
**TODO**: Give an overview of the deployed model and instructions on how to query the endpoint with a sample input.
from PIL import Image
import io
TODO: Run an prediction on the endpoint
with open("./dogImages/test/001.Affenpinscher/Affenpinscher_00003.jpg", "rb") as f:
    payload = f.read()
Image.open(io.BytesIO(payload))
response=predictor.predict(payload, initial_args={"ContentType": "image/jpeg"})
response


**TODO** Remember to provide a screenshot of the deployed active endpoint in Sagemaker.
in the file

## Standout Suggestions
**TODO (Optional):** This is where you can provide information about any standout suggestions that you have attempted.
