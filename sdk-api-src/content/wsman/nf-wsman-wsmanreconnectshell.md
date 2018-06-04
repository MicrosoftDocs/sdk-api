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

# WSManReconnectShell function


## -description


Reconnects a previously disconnected shell session. To reconnect the shell session's associated commands, use <a href="https://msdn.microsoft.com/3894BB74-4EAA-46D3-ACB2-AFDD3517A9C1">WSManReconnectShellCommand</a>.


## -parameters




### -param shell [in, out]

Specifies the handle returned by a call to the <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a> function. This parameter cannot be <b>NULL</b>.


### -param flags

This parameter is reserved for future use and must be set to zero.


### -param async [in]

Defines an asynchronous structure to contain an optional user context and a mandatory callback function. For more information, see  <a href="https://msdn.microsoft.com/9391e1a8-7048-49b8-9dc4-1da25b190238">WSMAN_SHELL_ASYNC</a>. This parameter cannot be <b>NULL</b>.


## -returns



This function does not return a value.



