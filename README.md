# aws-cdk-automation
Automating cloud services with aws cdk

## Getting Started
### Download Prerequisites
- [Nodejs](https://nodejs.org/en/download/) 
- [aws cli](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

For more details: [Prerequisites](https://docs.aws.amazon.com/cdk/v2/guide/getting_started.html#getting_started_prerequisites)

### Setting up environment
- Setup the virtual environment:
```shell script
    pip3 install --upgrade virtualenv
    virtualenv -p python3 venv
```
- Activate the venv and install requirements:
```shell script
    source venv/bin/activate
    pip install -r requirements.txt
```

### Configure AWS client
- setup iam user:
    - attach admin policy as this user is what we will use to interact with the cdk.
    - get access key and secret for the following step.
- configure aws cli:
```shell script
    aws configure
```

### AWS CDK
- install the cdk:
```shell script
    npm install -g aws-cdk
    cdk --version
```
- get account number and region:
```shell script
    aws sts get-caller-identity
```
- bootstrap:
```shell script
    cdk bootstrap aws://ACCOUNT-NUMBER/REGION
```

For more details: [AWS CDK](https://docs.aws.amazon.com/cdk/v2/guide/getting_started.html)
