# Structurizr Diagrams GitHub Actions Demo

This repository demonstrates the integration of two GitHub Actions for managing and commenting on Structurizr diagrams in pull requests. It is designed to automate the generation and display of Structurizr diagrams directly within GitHub's workflow.

## GitHub Actions Used

1. **Generate Structurizr Diagrams Images from DSL**: Automates the generation of Structurizr diagrams from DSL (Domain-Specific Language) files. [Action Marketplace Link](https://github.com/marketplace/actions/generate-structurizr-diagrams-images-from-dsl)

2. **Comment on PR with Structurizr Diagrams**: Automatically posts comment on pull request with previously generated Structurizr diagrams. [Action Marketplace Link](https://github.com/marketplace/actions/comment-on-pr-with-structurizr-diagrams)

These actions can be used together for a comprehensive workflow or independently.

## Workflows

### 1. Structurizr Diagrams Update

This workflow triggers on pull request events that include changes to the Structurizr DSL file. It uses the "Generate Structurizr Diagrams Images from DSL" action.

See: [`.github/workflows/structurizr-diagrams-update.yml`](.github/workflows/structurizr-diagrams-update.yml)


### 2. Structurizr Diagrams Comment

This workflow is triggered upon the completion of the Structurizr Diagrams Update workflow. It uses the "Comment on PR with Structurizr Diagrams" action.

See: [`.github/workflows/structurizr-diagrams-comment.yml`](.github/workflows/structurizr-diagrams-comment.yml)

## Docker Image

The first action utilizes a Docker image defined at: [sebastienfi/structurizr-cli-with-bonus](https://github.com/sebastienfi/structurizr-cli-with-bonus). It is built on top of the official image `structurizr/cli:latest` and adds the ability to generate diagrams images with PlantUML and commit to a git repository.

## Example Model

The demo generates diagrams for the official [Big Bank plc](https://structurizr.com/dsl?example=big-bank-plc) Structurizr C4 Architecture Model. The DSL file for this model is located at [`docs/workspace.dsl`](docs/workspace.dsl).

## Getting Started

To view these actions in action:

1. Make a change to the DSL file in this repository (e.g., modify `docs/workspace.dsl` to add a new relationship or modify a label or color).
2. Raise a pull request to see the actions in action!

## Contributing

Contributions to this demo are welcome. Please read our contributing guidelines to get started.