# README

```bash
aws cloudformation create-stack \
    --stack-name HelloWorldCodePipeline \
    --template-body file://template.yaml \
    --capabilities CAPABILITY_NAMED_IAM \
    --on-failure DELETE \
    --parameters ParameterKey=GitHubRepo,ParameterValue=hello-world \
                 ParameterKey=GitHubUser,ParameterValue=skehlet
```

```bash
aws cloudformation update-stack \
    --stack-name HelloWorldCodePipeline \
    --template-body file://template.yaml \
    --capabilities CAPABILITY_NAMED_IAM \
    --parameters ParameterKey=GitHubRepo,ParameterValue=hello-world \
                 ParameterKey=GitHubUser,ParameterValue=skehlet
```