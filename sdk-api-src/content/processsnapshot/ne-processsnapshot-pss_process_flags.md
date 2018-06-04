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

# PSS_PROCESS_FLAGS enumeration


## -description


Flags that describe a process.


## -enum-fields




### -field PSS_PROCESS_FLAGS_NONE

No flag.


### -field PSS_PROCESS_FLAGS_PROTECTED

The process is protected.


### -field PSS_PROCESS_FLAGS_WOW64

The process is a 32-bit process running on a 64-bit native OS.


### -field PSS_PROCESS_FLAGS_RESERVED_03

Undefined.


### -field PSS_PROCESS_FLAGS_RESERVED_04

Undefined.


### -field PSS_PROCESS_FLAGS_FROZEN

The process is frozen; for example,  a debugger is attached and broken into the process or a Store process is suspended by a lifetime management service.


## -remarks



There are <b>PSS_PROCESS_FLAGS</b> members in the <a href="https://msdn.microsoft.com/D629FA42-B501-4A0E-9B53-6D70E580B687">PSS_PROCESS_INFORMATION</a> and <a href="https://msdn.microsoft.com/F56E8C35-949A-4DEE-973F-CF24F6596036">PSS_HANDLE_ENTRY</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

