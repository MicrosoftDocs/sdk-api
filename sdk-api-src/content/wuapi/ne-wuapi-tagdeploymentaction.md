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

# tagDeploymentAction enumeration


## -description


Defines the action for which an update is explicitly deployed.


## -enum-fields




### -field daNone

No explicit deployment action is specified on the update. The update  inherits the value from its bundled updates.


### -field daInstallation

The update should be installed on the computer and/or for the specified user.


### -field daUninstallation

The update should be uninstalled from the computer and/or for the specified user.


### -field daDetection

The update is deployed only to determine the applicability of the update. The update will not be installed.

