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

# WSMAN_PLUGIN_RELEASE_COMMAND_CONTEXT callback function


## -description


Defines the release command callback for the plug-in. This function is called to delete the plug-in command context.

The DLL entry point name must be <b>WSManPluginReleaseCommandContext</b>.


## -parameters




### -param shellContext [in]

Specifies the context that was received when the shell was created.


### -param commandContext [in]

If this request is aimed at a command and not a shell, this is the context returned from the <b>winrm create</b> operation;  otherwise, this parameter is <b>NULL</b>.


## -returns



This callback function does not return a value.



