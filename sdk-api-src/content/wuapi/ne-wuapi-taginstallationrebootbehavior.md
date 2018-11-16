---
UID: NE:wuapi.tagInstallationRebootBehavior
title: tagInstallationRebootBehavior
author: windows-sdk-content
description: Defines the possible restart behaviors for an update.
old-location: wua\installationrebootbehavior.htm
tech.root: Wua_Sdk
ms.assetid: 28c5179a-bdfa-40ca-9cf2-239a9fbf5856
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: InstallationRebootBehavior, InstallationRebootBehavior [Windows Update Services], InstallationRebootBehavior enumeration [Windows Update Agent], irbAlwaysRequiresReboot, irbCanRequestReboot, irbNeverReboots, tagInstallationRebootBehavior, wua.installationrebootbehavior, wuapi/InstallationRebootBehavior, wuapi/irbAlwaysRequiresReboot, wuapi/irbCanRequestReboot, wuapi/irbNeverReboots
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - InstallationRebootBehavior
product: Windows
targetos: Windows
req.typenames: InstallationRebootBehavior
req.redist: 
---

# tagInstallationRebootBehavior enumeration


## -description


The <b>InstallationRebootBehavior</b> enumeration defines the possible restart behaviors for an update. The <b>InstallationRebootBehavior</b>  enumeration applies to the installation and uninstallation of updates.


## -enum-fields




### -field irbNeverReboots

The update never requires a system restart during or after an installation or an uninstallation.


### -field irbAlwaysRequiresReboot

The update always requires a system restart after a successful installation or uninstallation.


### -field irbCanRequestReboot

The update can request a system restart after a successful installation or uninstallation.

