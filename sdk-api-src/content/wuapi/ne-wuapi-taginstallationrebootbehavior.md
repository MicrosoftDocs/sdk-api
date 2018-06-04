---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

