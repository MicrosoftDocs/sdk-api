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

# _WTS_PROCESS_INFOW structure


## -description


Contains information about a process running on a Remote Desktop Session Host (RD Session Host) server.


## -struct-fields




### -field SessionId

Remote Desktop Services session identifier for the session associated with the process.


### -field ProcessId

Process identifier that uniquely identifies the process on the RD Session Host server.


### -field pProcessName

Pointer to a null-terminated string containing the name of the executable file associated with the process.


### -field pUserSid

Pointer to the user 
<a href="https://msdn.microsoft.com/7cb07bcd-70f4-43dd-8382-320fcff151c7">Security Identifiers</a> in the process's primary access token. For more information about SIDs and access tokens, see 
<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>.


## -see-also




<a href="https://msdn.microsoft.com/ddfae294-2e7c-416e-b328-76d011b4af39">WTSEnumerateProcesses</a>
 

 

