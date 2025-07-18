<!-- /docs/ is auto generated from the provider schema, and the templates in /templates do not edit files in /docs directly. -->

# SELECT Provider

The SELECT provider is used to manage resources in the [SELECT](https://select.dev) Snowflake optimization and cost management platform.

## Example Usage

```terraform
terraform {
  required_providers {
    select = {
      source  = "get-select/select"
      version = "~> 0.1"
    }
  }
}

provider "select" {
  api_key         = var.select_api_key
  organization_id = var.select_organization_id
}
```

## Authentication

The SELECT provider requires an API key and organization ID for authentication:

1. **API Key**: Generate an API key in the SELECT app:
   - Navigate to Settings → API Keys
   - Create a new API key with write permissions for the resources you would like to manage
   - Your API key will only be shown once and should be treated as a secret
   
2. **Organization ID**: Find your organization ID in the SELECT app:
   - Navigate to Settings → Profile Overview
   - Copy the organization ID

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `api_key` (String, Sensitive) API key for authentication with the Select API
- `organization_id` (String) Organization ID for the Select API

### Optional

- `select_api_url` (String) Base URL for the Select API 