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

# Toolhelp32ReadProcessMemory function


## -description


Copies memory allocated to another process into an application-supplied buffer.


## -parameters




### -param th32ProcessID [in]

The identifier of the process whose memory is being copied. This parameter can be zero to copy the memory of the current process.


### -param lpBaseAddress [in]

The base address in the specified process to read. Before transferring any data, the system verifies that all data in the base address and memory of the specified size is accessible for read access. If this is the case, the function proceeds. Otherwise, the function fails.


### -param lpBuffer [out]

A pointer to a buffer that receives the contents of the address space of the specified process.


### -param cbRead [in]

The number of bytes to read from the specified process.


### -param lpNumberOfBytesRead [out]

The number of bytes copied to the specified buffer. If this parameter is <b>NULL</b>, it is ignored.


## -returns



Returns <b>TRUE</b> if successful.




## -see-also




<a href="https://msdn.microsoft.com/097790e8-30c2-4b00-9256-fa26e2ceb893">Process32First</a>



<a href="https://msdn.microsoft.com/843a95fd-27ae-4215-83d0-82fc402b82b6">Process32Next</a>



<a href="https://msdn.microsoft.com/83732bd6-f4cf-409d-ad17-86503d408dc3">Tool Help Functions</a>
 

 

