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

# EngAllocUserMem macro


## -description


The <b>EngAllocUserMem</b> function allocates a block of memory from the address space of the current process and inserts a caller-supplied tag before the allocation.


## -parameters




### -param cj [in]

Specifies the number of bytes to allocate.


### -param tag [in]

Specifies a 4-byte <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">pool tag</a> that uniquely identifies the driver that does the memory allocation. For more information about pool tags, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544520">ExAllocatePoolWithTag</a>.


## -remarks



A process in an NT-based operating system has 4 GB of virtual address space. The upper 2 GB is system memory that is accessible only to kernel-mode threads; this space is identical across all processes. The lower 2 GB is user memory that is accessible to both user-mode and kernel-mode threads; this space is unique to its process. The memory allocated by <b>EngAllocUserMem</b> is allocated from the unique 2 GB of user memory, and is thus accessible only when the graphics driver is called in the context of the thread in which the memory was allocated. Graphics drivers always execute in the context of the caller; that is, graphics drivers cannot switch process contexts.

<b>EngAllocUserMem</b> is particularly useful to a printer driver with large bitmaps that will only be used by the current process. Rather than allocating from the system pool, this driver can instead allocate space from the current process's address space. Drivers need to exercise care with memory allocated by <b>EngAllocUserMem</b>, as it is possible for the application to alter this memory. <b>EngAllocUserMem</b> should only be used to allocate relatively large chunks of memory, as each allocation takes at least 64 KB of virtual address space. Sensitive data structures should never be allocated using this function. Also, user memory allocated by this function cannot be passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff565467">EngWritePrinter</a> by the printer driver.

When the memory is no longer needed, it can be freed by a call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564912">EngFreeUserMem</a> function.

To allocate user memory from the address space of a different process, use <a href="https://msdn.microsoft.com/library/windows/hardware/ff564177">EngAllocPrivateUserMem</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564177">EngAllocPrivateUserMem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564912">EngFreeUserMem</a>
 

 

