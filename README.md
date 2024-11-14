# CDK TypeScript playground project

Experimentation with the AWS CDK in TypeScript, including but not limited to layers
connectivity of components and security.

First pass associated with `Architecting on AWS` training, recreating many of the
concepts delivered in the training, but done via code instead of manually via AWS Console.

Remember: The `cdk.json` file tells the CDK Toolkit how to execute your app.

## Layers

The project has been split up into layers to help separate concerns within the project.  These layers are for
organisational purposes only.  

Rule of thumb: If a layer is changed and this forces a layer with a lower number to be changed then
this may be that the layers are incorrectly split.

## Useful commands

* `npm run build`   compile typescript to js
* `npm run watch`   watch for changes and compile
* `npm run test`    perform the jest unit tests
* `npx cdk deploy`  deploy this stack to your default AWS account/region
* `npx cdk diff`    compare deployed stack with current state
* `npx cdk synth`   emits the synthesized CloudFormation template

## Okta AWS CLI Login
[More details here](https://wiki.booking.com/pages/viewpage.action?pageId=1004409638)

Install okta-aws-cli
```shell
brew install okta-aws-cli
```

Get your AWS account credentials
```shell
okta-aws-cli --org-domain okta.booking.com --oidc-client-id 0oa69l79n9U8sx5if417 --aws-acct-fed-app-id 0oa1t1ub0fkS0kbyp416 --write-aws-credentials --open-browser
```
