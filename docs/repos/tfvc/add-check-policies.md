---
title: Add Check-In Policies
titleSuffix: Azure Repos
description: Add Check-In Policies
ms.assetid: 1f3046e3-1ea2-4477-99ca-76d3fc70c47b
ms.technology: devops-code-tfvc
ms.topic: conceptual
ms.date: 12/17/2021
monikerRange: '<= azure-devops'
---


# Add Check-In Policies

[!INCLUDE [temp](../includes/version-tfs-2013-cloud.md)]
[!INCLUDE [temp](../includes/version-vs-2013-vs-2019.md)]

Administrators of Team Foundation version control can add check-in policy requirements. These check-in policies require the user to take actions when they conduct a check-in to source control, for example a user can be required to associate a work item with a changeset. For more information about check-ins, see [Develop code and manage pending changes](develop-code-manage-pending-changes.md). By default, the following check-in policy types are available:

- **Builds**   Requires that the last build was successful before a check-in.
- **Code Analysis**   Requires that code analysis is run before check-in.
- **Work Items**   Requires that one or more work items be associated with the check-in.

> [!NOTE]
> For Visual Studio 2017 and later versions, Visual Studio check-in policies must be set through Team Explorer, tf.exe, or [through registry keys declared in the pkgdef of a Visual Studio extension](/visualstudio/extensibility/internals/createpkgdef-utility). Policies only apply to a single installation of Visual Studio on your computer. If you have multiple installations of Visual Studio, you'll need to set the check-in policy on each installation. For more information, see [What's New in the Visual Studio 2017 SDK?](/visualstudio/extensibility/what-s-new-in-the-visual-studio-2017-sdk) 


## To create a check-in policy

1.  From Team Explorer, select the **Settings** page, then select  **Source Control** under the **Project** section.

    The **Source Control Settings** dialog box appears.

2.  Click the **Check-in Policy** tab and then click **Add**.

    The **Add Check-in Policy** dialog box appears.

3.  In the Check-in Policy list, select the policy type you want and then click OK.

    The list includes the following selections:

    -   Select **Builds** if you want to require that a previous build was successful before any new changes can be checked in.

    -   Select **Code Analysis** if you want to require that code analysis is run before code can be checked in. The **Code Analysis Policy Editor** dialog box appears.

        Select the check boxes for the types of code analysis that you want performed. Options are Enforce check-in to only contain files that are part of current solution, **Enforce C/C++ Code Analysis (/analyze)**, and **Enforce Code Analysis For Managed Code**. If you select the **Enforce Code Analysis For Managed Code** check box, select the desired rule settings under **Rule settings for Managed Code Analysis**.

        For more information about how to use code analysis tools, see [Create Code Analysis Check-In Policies](/visualstudio/code-quality/how-to-create-or-update-standard-code-analysis-check-in-policies).

        When you are finished, click **OK**.

    -   If you selected **Work Items**, the policy is added to the list that a work item must be associated with the check in.

4.  When you are satisfied with the settings for the check-in policies, click **OK**; the new check-in policy now displays with future check-ins.

## Related articles 

- [Configure command](configure-command.md)
- [Set and enforce quality gates](set-enforce-quality-gates.md)
- [Walkthrough: Customizing checkin policies and notes](/previous-versions/ms181281(v=vs.100))