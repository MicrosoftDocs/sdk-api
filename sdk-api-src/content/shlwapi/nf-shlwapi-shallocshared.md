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

# SHAllocShared function


## -description


<p class="CCE_Message">[<b>SHAllocShared</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Allocates a handle in a specified process to a copy of a specified memory block in the calling process.


## -parameters




### -param pvData [in, optional]

Type: <b>const void*</b>

A pointer to the memory block in the calling process that is to be copied. You can set this parameter to <b>NULL</b> if you want to share a block of memory without copying any data to it.


### -param dwSize [in]

Type: <b>DWORD</b>

The size, in bytes, of the memory block pointed to by <i>pvData</i>.


### -param dwProcessId

TBD




#### - dwDestinationProcessId [in]

Type: <b>DWORD</b>

The process ID of the process that will share memory block specified by <i>pvData</i>.


## -returns



Type: <b>HANDLE</b>

Returns a handle to the shared memory for the process specified by <i>dwDestinationProcessId</i>. Returns <b>NULL</b> if unsuccessful.




## -remarks



Use <a href="https://msdn.microsoft.com/5a86ae5d-8caa-4126-a22e-bc3cc7df2381">SHFreeShared</a> to free the handle when you are finished.




## -see-also




<a href="https://msdn.microsoft.com/5a86ae5d-8caa-4126-a22e-bc3cc7df2381">SHFreeShared</a>



<a href="https://msdn.microsoft.com/5b948044-6cec-4649-a266-21959154f999">SHLockShared</a>



<a href="https://msdn.microsoft.com/8ecbf62b-fd0d-4a8d-bd55-42c0c3f64390">SHUnlockShared</a>
 

 

