# Synapse-Onyphe Rapid Power-Up

**Synapse-Onyphe** is a Rapid Power-Up for Synapse, designed to enhance your
cybersecurity and threat intelligence workflows by seamlessly integrating with
the Onyphe platform. Onyphe is a comprehensive Cyber Defense Search Engine that
excels in Attack Surface Discovery and Management, making it an invaluable tool
for security professionals.

With the Synapse-Onyphe Rapid Power-Up, you can effortlessly query Onyphe's
vast repository of information and leverage its insights directly within your
Synapse environment. This README will guide you through the installation
process and provide examples of how to harness the power of Synapse-Onyphe.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you can make use of Synapse-Onyphe, ensure that you have the following
prerequisites in place:

1. **Synapse**: You must have a functioning installation of Synapse. If you
haven't already, refer to the Synapse documentation for installation
instructions.

2. **Onyphe API Key**: To access Onyphe's features, you need a valid Onyphe API
key. If you don't have one, visit the Onyphe website to obtain your API key.

## Installation from source

Installing the Synapse-Onyphe Rapid Power-Up is a straightforward process.
Follow these steps:

1. **Clone the Repository**: Clone this repository to your Synapse environment
   using Git or download it as a ZIP archive and extract it.

2. **Deploy the Power-Up**: Copy the `synapse-onyphe` directory to your Synapse
   Power-Ups directory. The location may vary depending on your Synapse
   installation.

   ```
   python -m synapse.tools.genpkg ./synapse-onyphe.yaml \
     --push tcp://USER:PASSWORD@localhost/cortex
   ```

3. **Configuration**: Configure the Power-Up by providing your Onyphe API key.
   You can do this by running a configuration command. Refer to the
   [Usage](#usage) section for details.

## Usage

Once Synapse-Onyphe is installed and configured, you can use it to query Onyphe
directly from your Synapse environment. Here are some essential commands and
usage instructions:

- **Configuring your Onyphe API Key**: Use the following command to set your
  Onyphe API key:

  ```
  > cyl.onyphe.setup.apikey --self <your_api_key>
  ```

- **Querying Onyphe**: To perform queries using Onyphe, you can use commands
  provided by this Power-Up. Refer to the [Examples](#examples) section for
  sample queries.

## Examples

Let's explore a few examples of how to use Synapse-Onyphe:

- **Querying for IP Information**: Retrieve detailed information about a
  specific IP address using the Onyphe Power-Up.

  ```
  > cyl.onyphe.search --query 'ip:8.8.8.8' --yield
  ```

- **Searching for Domains**: Perform domain-based searches with Onyphe to
  gather threat intelligence.

  ```
  > cyl.onyphe.search --query 'domain:google.com' --yield
  ```

These are just a few examples of what you can achieve with Synapse-Onyphe.
Refer to the documentation for more advanced queries and options.

## Contributing

We welcome contributions from the community to improve and expand the
capabilities of Synapse-Onyphe. If you have ideas, bug reports, or feature
requests, please feel free to open an issue or submit a pull request in this
repository.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use,
modify, and distribute it in accordance with the terms of the license.

---

Thank you for using Synapse-Onyphe! We hope this Power-Up enhances your
cybersecurity efforts and threat intelligence workflows. 