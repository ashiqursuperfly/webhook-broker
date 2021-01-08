# AWS Infrastructure

This Terraform configuration provides a infrastructure as a code for Webhook Broker in AWS.

## Usage

Please make sure to create a `custom_vars.auto.tfvars` file with the following variables to use Client VPN [module](./modules/client-vpn/README.md).

```terraform
vpn_server_cert_arn = "arn:aws:acm:<REGION>:<ACCOUNT_ID>:certificate/<CERT_ARN_FOR_SERVER>"
vpn_client_cert_arn = "arn:aws:acm:<REGION>:<ACCOUNT_ID>:certificate/<CERT_ARN_FOR_CLIENT>"
```

Once you apply the config, it will generate a `config.ovpn` file for connecting to VPN; make sure to edit it as per Client VPN [README](./modules/client-vpn/README.md).