# Unreal Engine Jenkins Pipeline

## Description
This repo serves as a Unreal Engine Jenkins pipeline for a project I was involved in. The Repo can be replaced with any Unreal Engine Repo, although you may need to change .NET SDK or Unreal Engine version to make it compatible.
In it's current state, it will pull from a branch, build it, zip it, upload to google drive (provided the RCLONE config has been updated to do so) and increment the build version.

### How To Setup
- Install Windows Server on a VM / Local Machine
- Install [Jenkins](https://www.jenkins.io/) on that server
- Install [Git](https://git-scm.com/)
- Download [Rclone](https://rclone.org/downloads/) place binary at C:\
  - Create Environment Variable for Rclone in Windows
  - Create a token and build config with rclone for google drive

  PS C:\Users\Administrator> rclone config show
  [WS]
  type = drive
  scope = drive
  token = <token>
  team_drive =

PS C:\Users\Administrator>
- Create Rclone Config
- Install [Visual Studio 2022] (https://dev.epicgames.com/community/learning/tutorials/XjvJ/unreal-engine-fab-ue-5-1-visual-studio-2022-installation-guide)
- Install [Epic Games Store] (https://store.epicgames.com/)
- Install Unreal Engine 5.8 From inside Epic Games Store
- Install [.NET SDK 10.0] (https://dotnet.microsoft.com/en-us/download/dotnet/10.0)
- Setup Jenkins
- Create a new Pipeline, use the pipeline in the repo in Groovy (make sure the references match where you want the files to be)
