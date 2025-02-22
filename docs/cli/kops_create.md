
<!--- This file is automatically generated by make gen-cli-docs; changes should be made in the go CLI command code (under cmd/kops) -->

## kops create

Create a resource by command line, filename or stdin.

### Synopsis

Create a resource:
        
  *  cluster
  *  instancegroup
  *  secret

 Create a cluster, instancegroup, keypair, or secret using command line parameters, YAML configuration specification files, or stdin. (Note: keypairs and secrets cannot be created from YAML config files yet).

```
kops create {-f FILENAME}... [flags]
```

### Examples

```
  # Create a cluster from the configuration specification in a YAML file.
  kops create -f my-cluster.yaml
  
  # Create secret from secret spec file.
  kops create -f secret.yaml
  
  # Create an instancegroup based on the YAML passed into stdin.
  cat instancegroup.yaml | kops create -f -
```

### Options

```
  -f, --filename strings   Filename to use to create the resource
  -h, --help               help for create
```

### Options inherited from parent commands

```
      --config string   yaml config file (default is $HOME/.kops.yaml)
      --name string     Name of cluster. Overrides KOPS_CLUSTER_NAME environment variable
      --state string    Location of state storage (kops 'config' file). Overrides KOPS_STATE_STORE environment variable
  -v, --v Level         number for the log level verbosity
```

### SEE ALSO

* [kops](kops.md)	 - kOps is Kubernetes Operations.
* [kops create cluster](kops_create_cluster.md)	 - Create a Kubernetes cluster.
* [kops create instancegroup](kops_create_instancegroup.md)	 - Create an instancegroup.
* [kops create keypair](kops_create_keypair.md)	 - Add a CA certificate and private key to a keyset.
* [kops create secret](kops_create_secret.md)	 - Create a secret.
* [kops create sshpublickey](kops_create_sshpublickey.md)	 - Create an SSH public key.

