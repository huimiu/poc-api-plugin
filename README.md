# Overview of API Plugin from Scratch Template

## Known issues
Currently, this project is unable to run successfully.
- The Teams manifest schema hasn't been finalized yet. As a result, some actions in the teamsapp.local.yaml and teamsapp.yaml files may fail to execute, such as `validateManifest`, `validateAppPackage` and `extendToM365`.
- This POC is built based on the latest known [Type B schema](https://spec-hub.azurewebsites.net/specifications/PluginManifest-2.0.html#plugin-manifest-object). If there are changes to the definition of the Type B schema in the future, corresponding updates may be required.

## Build an API Plugin from a new API with Azure Functions

This app template allows Teams to interact directly with third-party data, apps, and services, enhancing its capabilities and broadening its range of capabilities. It allows Teams to:

- Retrieve real-time information, for example, latest news coverage on a product launch.
- Retrieve knowledge-based information, for example, my team’s design files in Figma.

## Get started with the template

> **Prerequisites**
>
> To run this app template in your local dev machine, you will need:
>
> - [Node.js](https://nodejs.org/), supported versions: 16, 18
> - A [Microsoft 365 account for development](https://docs.microsoft.com/microsoftteams/platform/toolkit/accounts)
> - [Teams Toolkit Visual Studio Code Extension](https://aka.ms/teams-toolkit) version 5.0.0 and higher or [Teams Toolkit CLI](https://aka.ms/teamsfx-cli)

1. First, select the Teams Toolkit icon on the left in the VS Code toolbar.
2. In the Account section, sign in with your [Microsoft 365 account](https://docs.microsoft.com/microsoftteams/platform/toolkit/accounts) if you haven't already.
3. Select `Debug in Teams (Edge)` or `Debug in Teams (Chrome)` from the launch configuration dropdown.
4. Send a message to Copilot to find a repair record.


## What's included in the template

| Folder       | Contents                                                                                                    |
| ------------ | ----------------------------------------------------------------------------------------------------------- |
| `.vscode`    | VSCode files for debugging                                                                                  |
| `appPackage` | Templates for the Teams application manifest, the API specification and response template for API responses |
| `env`        | Environment files                                                                                           |
| `infra`      | Templates for provisioning Azure resources                                                                  |
| `repair`     | The source code for the repair API                                                                          |

The following files can be customized and demonstrate an example implementation to get you started.

| File                                         | Contents                                                                     |
| -------------------------------------------- | ---------------------------------------------------------------------------- |
| `src/functions/repair.ts`                    | The main file of a function in Azure Functions.                     |
| `src/repairsData.json`                       | The data source for the repair API.                                 |
| `appPackage/apiSpecificationFile/repair.yml` | A file that describes the structure and behavior of the repair API.          |
| `appPackage/ai-plugin.json`                  | The manifest file for the API plugin.                                        |
| `repairsData.json`                           | The data source for the repair API                                           |

The following are Teams Toolkit specific project files. You can [visit a complete guide on Github](https://github.com/OfficeDev/TeamsFx/wiki/Teams-Toolkit-Visual-Studio-Code-v5-Guide#overview) to understand how Teams Toolkit works.

| File                 | Contents                                                                                                                                  |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `teamsapp.yml`       | This is the main Teams Toolkit project file. The project file defines two primary things: Properties and configuration Stage definitions. |
| `teamsapp.local.yml` | This overrides `teamsapp.yml` with actions that enable local execution and debugging.                                                     |
