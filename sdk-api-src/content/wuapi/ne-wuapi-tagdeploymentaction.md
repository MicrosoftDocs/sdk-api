---
UID: NE:wuapi.tagDeploymentAction
title: tagDeploymentAction
author: windows-sdk-content
description: Defines the action for which an update is explicitly deployed.
old-location: wua\deploymentaction.htm
old-project: wua_sdk
ms.assetid: c192db44-05ad-4fb2-aa51-9153389d95dc
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DeploymentAction, DeploymentAction enumeration [Windows Update Agent], daDetection, daInstallation, daNone, daUninstallation, tagDeploymentAction, wua.deploymentaction, wuapi/DeploymentAction, wuapi/daDetection, wuapi/daInstallation, wuapi/daNone, wuapi/daUninstallation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wuapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DeploymentAction
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - DeploymentAction
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

