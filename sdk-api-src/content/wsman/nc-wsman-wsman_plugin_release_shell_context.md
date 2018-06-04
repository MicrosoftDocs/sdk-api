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

# WSMAN_PLUGIN_RELEASE_SHELL_CONTEXT callback function


## -description


Defines the release shell callback for the plug-in. This function is called to delete the plug-in shell context.

The DLL entry point name must be <a href="https://msdn.microsoft.com/9a81f8da-1c71-4eab-aa21-002cee4f1164">WSManPluginReleaseCommandContext</a>.


## -parameters




### -param shellContext [in]

Specifies the context that was received when the shell was created.


## -returns



This callback function does not return a value.



