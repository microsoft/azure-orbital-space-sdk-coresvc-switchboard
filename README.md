# Switchboard

[![coresvc-switchboard-build](https://github.com/microsoft/azure-orbital-space-sdk-coresvc-switchboard/actions/workflows/coresvc-switchboard-build.yml/badge.svg)](https://github.com/microsoft/azure-orbital-space-sdk-coresvc-switchboard/actions/workflows/coresvc-switchboard-build.yml)

Switchboard is the Azure Orbital Space SDK's MQTT router.  Switchboard builds [rabbitMQ](https://github.com/rabbitmq/rabbitmq-server) from source with updates to source images from the Microsoft Container Registry.

## Build

```bash
# Download the Azure Orbital Space SDK Setup scripts via the devcontainer feature
devcontainer up --workspace-folder ${PWD}

# or alternatively, clone the Azure Orbital Space SDK Setup repo and run copy_to_spacedev.sh
# git clone https://github.com/microsoft/azure-orbital-space-sdk-setup && cd azure-orbital-space-sdk-setup && ./.vscode/copy_to_spacedev.sh



bash /var/spacedev/build/build_containerImage.sh --dockerfile Dockerfiles/Dockerfile --image-tag 0.11.0 --architecture amd64 --repo-dir ${PWD} --app-name coresvc-switchboard --annotation-config azure-orbital-space-sdk-coresvc-switchboard.yaml

bash /var/spacedev/build/build_containerImage.sh --dockerfile Dockerfiles/Dockerfile --image-tag 0.11.0 --architecture arm64 --repo-dir ${PWD} --app-name coresvc-switchboard --annotation-config azure-orbital-space-sdk-coresvc-switchboard.yaml
```

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft
trademarks or logos is subject to and must follow
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
