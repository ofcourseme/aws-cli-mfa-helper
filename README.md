# aws-cli-mfa-token-generator

Bored of manually generating and setting MFA Session Token for aws-cli? Yeah me too

This script will automatically generate those tokens and change your `default` aws configuration with the right values

## Setup

1) Define a `mfa-base` configuration profile for aws-cli with at least your `AWS Access Key ID` and `AWS Secret Access Key`

    ```sh
    aws configure --profile mfa-base
    ```

2) Set your MFA ARN in the mfa-base configuration

    ```sh
    aws configure set aws_mfa_arn <yourawsmfaarn> --profile mfa-base
    ```

## Usage

Just launch the script with `./generateAWStoken.sh` (of add it to your path somehow with a better name) and type the OPT code when prompted
