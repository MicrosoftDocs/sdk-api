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

# WSManConnectShellCommand function


## -description


Connects to an existing  command running in a shell.


## -parameters




### -param shell [in, out]

Specifies the shell handle returned by the <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a> call. This parameter cannot be <b>NULL</b>.


### -param flags

Reserved for future use. Must be zero.


### -param commandID [in]

A null-terminated string that identifies a specific command, currently running in the server session, that the client intends to connect to.


### -param options [in, optional]

Defines a set of options for the command. These options are passed to the service to modify or refine the command execution. This parameter can be <b>NULL</b>. For more information about the options, see <a href="https://msdn.microsoft.com/16a1447c-d764-44bf-9c62-064769ead0f3">WSMAN_OPTION_SET</a>.


### -param connectXml [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/4ff574d4-04b0-47c3-808f-867d6815bffc">WSMAN_DATA</a> structure that defines an open context for the connect shell operation. The content must be a valid XML string. This parameter can be <b>NULL</b>.


### -param async [in]

Defines an asynchronous structure to contain an optional user context and a mandatory callback function. For more information, see <a href="https://msdn.microsoft.com/9391e1a8-7048-49b8-9dc4-1da25b190238">WSMAN_SHELL_ASYNC</a>. This parameter cannot be <b>NULL</b>.


### -param command [out]

This handle is returned on a successful call and is used to send and receive data and to signal the command. When you have finished using this handle, close it by calling the <a href="https://msdn.microsoft.com/41ef2a6d-af1a-4a51-b01d-262380f01187">WSManCloseCommand</a> method. This parameter cannot be <b>NULL</b>.


## -returns



This function does not return a value.



