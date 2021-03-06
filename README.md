# Terraform - GKE Cluster Deployment

## Versions

| Name | Version |
|------|---------|
| terraform | >= 0.13.0|

## Inputs - terraform.tfvars

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| cluster_name | cluster Name | `string` | `{}` | yes |
| project_id | project id to deploy the cluster | `string` | `{}` | yes |
| gke_num_nodes | default nodes number 1| `number` | `{}` | no |
| image | default image - ubuntu | `string` | `{}` | no |

## Outputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| GKE Cluster Name | Cluster Name | `string` | `{}` | yes |
| GKE Cluster Endpoint | Cluster Endpoint | `string` | `{}` | yes |

### How to deploy

- Create the terraform vars file:

## file - terraform.tfvars
```
cluster_name = "nvlabs"
project_id = "your-project-id"
```
## Deploy and Manage your deployment using terraform:
    - init your plugins                 ```terraform init```
    - plan your deployment              ```terraform plan```
    - apply the changes in your cluster ```terraform apply```

## Connect to the Cluster
```
gcloud container clusters get-credentials [CLUSTE_NAME] --zone [ZONE] --project [PROJECT_NAME]
```

### Clean Up
- destroy your deployment: ```terraform destroy```
