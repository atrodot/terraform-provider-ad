<a href="https://terraform.io">
    <img src="https://github.com/hashicorp/terraform-provider-azurerm/raw/main/.github/tf.png" alt="Terraform logo" title="Terraform" align="left" height="50" />
</a>

# Terraform Provider for Windows Active Directory (AD)

[![Releases](https://img.shields.io/github/release/atrodot/terraform-provider-ad.svg)](https://github.com/atrodot/terraform-provider-ad/releases)
[![LICENSE](https://img.shields.io/github/license/atrodot/terraform-provider-ad.svg)](https://github.com/atrodot/terraform-provider-ad/blob/main/LICENSE)
[![Registry](https://img.shields.io/badge/terraform-registry-blue)](https://registry.terraform.io/providers/atrodot/ad/latest)

This is a community-maintained fork of the [HashiCorp AD provider](https://github.com/hashicorp/terraform-provider-ad) (now archived). It allows you to manage users, groups, and group policies in your Active Directory installation.

## What's New in This Fork

* **`cn` (Common Name) attribute** on `ad_user` — explicitly set the AD object's CN independently of `display_name`
* **Go 1.26.0** — updated from Go 1.21
* **GitHub Actions CI** — automated releases via GoReleaser with GPG signing
* Published to the [Terraform Registry](https://registry.terraform.io/providers/atrodot/ad/latest)

## Requirements

* [Terraform](https://www.terraform.io/downloads.html) version 0.12.x+
* [Windows Server](https://www.microsoft.com/en-us/windows-server) 2012R2 or greater
* [Go](https://golang.org/doc/install) version 1.26.x+ (for building from source)

## Getting Started

Install the provider from the [Terraform Registry](https://registry.terraform.io/providers/atrodot/ad/latest):

```hcl
terraform {
  required_providers {
    ad = {
      source  = "atrodot/ad"
      version = "~> 0.6.0"
    }
  }
}
```

Then review the [docs](docs/) folder for configuration options and [examples](examples/) for usage patterns. Run `terraform init` to download the provider.

## Contributing

We welcome contributions. If you have an idea for an enhancement or bug fix, please first [create an issue](https://github.com/atrodot/terraform-provider-ad/issues/new/choose) so we can discuss the implementation before you proceed.

You can review our [contribution guide](_about/CONTRIBUTING.md) and [FAQ](_about/FAQ.md).
