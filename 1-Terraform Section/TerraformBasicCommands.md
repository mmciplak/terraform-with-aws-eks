**init:** The terraform init command initializes a working directory containing Terraform configuration files. This is the first command that should be run after writing a new Terraform configuration or cloning an existing one from version control. It is safe to run this command multiple times.

validate: The terraform validate command validates the configuration files in a directory, referring only to the configuration and not accessing any remote services such as remote state, provider APIs, etc.

plan: The terraform plan command creates an execution plan, which lets you preview the changes that Terraform plans to make to your infrastructure. By default, when Terraform creates a plan it:

    -Reads the current state of any already-existing remote objects to make sure that the Terraform state is up-to-date.
    -Compares the current configuration to the prior state and noting any differences.
    -Proposes a set of change actions that should, if applied, make the remote objects match the configuration.

apply: The terraform apply command executes the actions proposed in a Terraform plan.

destroy: The terraform destroy command is a convenient way to destroy all remote objects managed by a particular Terraform configuration.

    -While you will typically not want to destroy long-lived objects in a production environment, Terraform is sometimes used to manage ephemeral infrastructure for development purposes, in which case you can use terraform destroy to conveniently clean up all of those temporary objects once you are finished with your work.