---
UID: NF:memoryapi.QueryMemoryResourceNotification
title: QueryMemoryResourceNotification function
author: windows-sdk-content
description: Retrieves the state of the specified memory resource object.
old-location: base\querymemoryresourcenotification.htm
tech.root: memory
ms.assetid: 95a38b97-7fae-4ec6-aa9e-cc800d40594b
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: QueryMemoryResourceNotification, QueryMemoryResourceNotification function, _win32_querymemoryresourcenotification, base.querymemoryresourcenotification, winbase/QueryMemoryResourceNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - QueryMemoryResourceNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- QueryMemoryResourceNotification
: 
---

# QueryMemoryResourceNotification function


## -description


Retrieves the state of the specified memory resource object.


## -parameters




### -param ResourceNotificationHandle [in]

A handle to a memory resource notification object. The 
<a href="https://msdn.microsoft.com/e4d794ca-4abb-4933-bd07-793e78c52881">CreateMemoryResourceNotification</a> function returns this handle.


### -param ResourceState [out]

The memory pointed to by this parameter receives the state of the memory resource notification object. The value of this parameter is set to <b>TRUE</b> if the specified memory condition exists, and  <b>FALSE</b> if the specified memory condition does not exist.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. For more error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Unlike the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>, 
<b>QueryMemoryResourceNotification</b> does not block the calling thread. Therefore, it is an efficient way to check the state of physical memory before proceeding with an operation.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/e4d794ca-4abb-4933-bd07-793e78c52881">CreateMemoryResourceNotification</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>
 

 

