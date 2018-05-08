---
UID: TP:wsl
ms.assetid: 6050dbda-ec04-3dd4-a492-e2713ff71245
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Windows Subsystem for Linux



Overview of the Windows Subsystem for Linux technology.

To develop Windows Subsystem for Linux, you need these headers:

 * [wslapi.h](..\wslapi\index.md)

For the programming guide, see [Windows Subsystem for Linux](https://review.docs.microsoft.com/en-us/win32-test/wsl).

## Functions

| Title   | Description   |
| ---- |:---- |
| [WslConfigureDistribution function](..\wslapi\nf-wslapi-wslconfiguredistribution.md) | Modifies the behavior of a distribution registered with the Windows Subsystem for Linux (WSL). |
| [WslGetDistributionConfiguration function](..\wslapi\nf-wslapi-wslgetdistributionconfiguration.md) | Retrieves the current configuration of a distribution registered with the Windows Subsystem for Linux (WSL). |
| [WslIsDistributionRegistered function](..\wslapi\nf-wslapi-wslisdistributionregistered.md) | Determines if a distribution is registered with the Windows Subsystem for Linux (WSL). |
| [WslLaunch function](..\wslapi\nf-wslapi-wsllaunch.md) | Launches a Windows Subsystem for Linux (WSL) process in the context of a particular distribution. |
| [WslLaunchInteractive function](..\wslapi\nf-wslapi-wsllaunchinteractive.md) | Launches an interactive Windows Subsystem for Linux (WSL) process in the context of a particular distribution. |
| [WslRegisterDistribution function](..\wslapi\nf-wslapi-wslregisterdistribution.md) | Registers a new distribution with the Windows Subsystem for Linux (WSL). |
| [WslUnregisterDistribution function](..\wslapi\nf-wslapi-wslunregisterdistribution.md) | Unregisters a distribution from the Windows Subsystem for Linux (WSL). |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [WSL_DISTRIBUTION_FLAGS enumeration](..\wslapi\ne-wslapi-wsl_distribution_flags.md) | The WSL_DISTRIBUTION_FLAGS enumeration specifies the behavior of a distribution in the Windows Subsystem for Linux (WSL). |
