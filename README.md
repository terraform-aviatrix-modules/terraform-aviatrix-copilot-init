# terraform-aviatrix-copilot-init

### Description
This module initializes a freshly deployed copilot.

### Compatibility
Module version | Terraform version
:--- | :---
v1.0.0 | >= 1.3

### Usage Example
```hcl
module "copilot_init" {
  source  = "terraform-aviatrix-modules/copilot-init/aviatrix"
  version = "1.0.0"

  avx_controller_public_ip         = "1.2.3.4"
  avx_controller_admin_password    = "mysecretpassword"
  avx_copilot_public_ip            = "2.3.4.5"
  account_email                    = "admin@domain.com"
  copilot_service_account_password = "mysecretpassword"
}
```

### Variables
The following variables are required:

key | value
:--- | :---
avx_controller_public_ip | Public IP of the controller
avx_controller_admin_password | Admin password for the controller
avx_copilot_public_ip | Public IP of Copilot
service_account_email | Email address for the service account
copilot_service_account_password | Desired password for the service account

The following variables are optional:

key | default | value 
:---|:---|:---
avx_controller_admin_username | Admin username for the controller | admin
copilot_service_account_username | Service account name for Copilot | copilot_service_account

### Outputs
This module will return the following outputs:

key | description
:---|:---
copilot_init_simple_result | Result of the copilot initialization
