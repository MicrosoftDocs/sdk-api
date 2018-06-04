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

# SHLockShared function


## -description


<p class="CCE_Message">[<b>SHLockShared</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Maps a block of memory from a specified process into the calling process.


## -parameters




### -param hData [in]

Type: <b>HANDLE</b>

A handle to the memory you want to map into the calling process.


### -param dwProcessId [in]

Type: <b>DWORD</b>

The process ID of the process from which you want to map the block of memory.


## -returns



Returns a void pointer to the shared memory. Returns <b>NULL</b> if unsuccessful.




## -remarks



Call <a href="https://msdn.microsoft.com/8ecbf62b-fd0d-4a8d-bd55-42c0c3f64390">SHUnlockShared</a> to unlock the memory that this function maps. Call <a href="https://msdn.microsoft.com/5a86ae5d-8caa-4126-a22e-bc3cc7df2381">SHFreeShared</a> to release the memory.



