---
title: Account Usage
description: Explore how to configure your Daytona account to your needs.
sidebar:
  label: Account
---

Each Daytona account can be configured to your needs, enhancing productivity and usability through setting global dotfiles, environment variables, and SSH keys, and an editor for your workspaces.
You can connect your account to additional Git providers for even more flexibility in accessing projects across your organization.

## Profile

The Daytona profile section provides essential user information and includes the following key elements:

- **User ID**

    A unique, system-generated identifier that is automatically assigned to each user. This value is permanent and cannot be modified by the user.

- **Name**

    The user's display name, which is visible to other users within the system. This name represents the user in all interactions.

- **Email**

    The primary email address linked to the user’s account. This email is used for account-related communications and notifications.

In the dashboard, navigate to your profile account icon and select **`Profile`** to access your user information.

## Settings

The Daytona settings profile section enables you to manage integrations, preferences, and account actions. It provides information on managing Git Providers permissions, choosing the default code editor (IDE) for opening development Workspaces, entering the URL of a repository that includes dotfiles, selecting a theme preference, and deleting an account.

In the dashboard, navigate to your profile account icon and select **`Settings`** to manage integrations, preferences, and account actions.

- **Git Providers**

    Manage permissions and connections to Git providers. Options include connecting to external Git services (e.g., Not connected) or self-managed Git environments.

- **Default IDE**

    Select the preferred code editor (IDE) for opening Workspaces.

- **Dotfiles**

    Specify the URL of a repository containing dotfiles. These files will be automatically cloned and applied in every Workspace.

- **Theme Preference**

    Choose a color theme or sync with the system settings to automatically switch between light and dark modes (e.g., system mode).

- **Delete Account**

    Permanently delete the account and all associated data, including workspaces. Note that this action is irreversible.

## Notifications

The Daytona notifications section provides options to view alerts and updates related to your account activities.

In the dashboard, navigate to your profile account icon and select **`Notifications`** to view alerts and updates related to your account activities.

## Environment Variables

The Daytona environments variables section provides an option to add an environment variable to be available across your Workspaces.

1. In the dashboard, navigate to your profile account icon and select **`Env Variables`** to add an environment variable.
2. Select **`New +`** to add a new environment variable.
3. Enter the environment variable `name` and `value`.

:::note
Environment variable names must consist solely of uppercase letters, digits and underscores, but must not start with a digit.

While setting an expiration date for your key is optional, it is good practice to set this date and rotate SSH keys periodically.
:::


:::tip
To set configuration for your environment using dotfiles, see *[Configuring the default dotfiles repository for new workspaces](#configuring-the-default-dotfiles-repository-for-new-workspaces)*.
:::

## SSH Keys

The Daytona SSH keys section provides an option to add a new SSH key for authentication purposes and configure public keys associated with your account.

1. In the dashboard, navigate to your profile account icon and select **`SSH Keys`** to add an SSH key.
2. Select **`New +`** to add a new SSH key.
3. Enter the SSH key `name`, `key`, and `expiration date`.

:::caution
Key names are publicly visible.
:::

## About

The Daytona about section provides an overview of the associated license and current version of the Daytona.

- **License**

    The license tier your Daytona account is associated with.

- **Version**

    The version of Daytona you are using.


## Adding Dotfiles

You can configure new workspaces to be populated with a set of dotfiles at creation time using the Daytona dashboard.

After setting a Git repository for dotfiles, Daytona will clone the repository into the home directory of each new workspace.
This allows you to share a common set of configuration across your workspaces.
Examples of potential configuration include shell configuration (`~/.bashrc`, `~/.profile`) and CLI tool configuration in `~/.config/`.

:::note
To use this feature, you need the URL of a Git repository with your desired dotfiles.
:::

<br />

:::tip
To set individual environment variables directly in the Daytona dashboard, see *[Sharing a common environment variable across workspaces](#sharing-a-common-environment-variable-across-workspaces)*.
:::

<br />

1. Navigate to the *Settings* page under *Account* in the sidebar.
2. Under *Dotfiles*, specify the URL of the Git repository containing your dotfiles.
3. Click the `Update` button to save the configuration.
