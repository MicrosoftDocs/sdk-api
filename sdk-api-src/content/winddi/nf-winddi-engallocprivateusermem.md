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

# EngAllocPrivateUserMem macro


## -description


The <b>EngAllocPrivateUserMem</b> function allocates a block of user memory from the address space of a specified process and inserts a caller-supplied tag before the allocation.


## -parameters




### -param psl [in]

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure representing the Microsoft DirectDraw surface with which to associate the allocated memory.


### -param cj [in]

Specifies the number of bytes of memory to allocate.


### -param tag [in]

Specifies a 4-byte <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">pool tag</a> that uniquely identifies the driver that does the memory allocation. For more information about pool tags, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544520">ExAllocatePoolWithTag</a>.


## -remarks



A DirectDraw driver might require a user-memory "scratch pad" in place of true video memory. Although this practice is discouraged due to its performance implications, it is occasionally necessary. This scratch memory is usually allocated only for a short period of time. After the memory has been allocated, it is used for the intended graphics operations, and then deallocated.

A problem arises if the driver instance is destroyed before the surface is unlocked. A particular case occurs when the system switches to a protected desktop as a result of a user pressing CTRL+ALT+DEL. In this situation, the mode switch is performed on a system process context. If the driver has any outstanding surface locks, such as when the mode switch happens before the surface has been unlocked, the driver will be required to destroy that surface on a different process context. The driver cannot call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564912">EngFreeUserMem</a> to deallocate the scratch memory since this entry point will fail if called on a different context from that used when the memory was allocated.

<b>EngAllocPrivateUserMem</b>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff564907">EngFreePrivateUserMem</a> are provided to address this problem. These two functions are identical to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564178">EngAllocUserMem</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff564912">EngFreeUserMem</a>, except that they do the extra work required to free memory allocated on a different process context. Process context information is stored with the DirectDraw object that owns the DirectDraw surface object to which <i>psl</i> points.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551726">DD_SURFACE_GLOBAL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564178">EngAllocUserMem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564907">EngFreePrivateUserMem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564912">EngFreeUserMem</a>
 

 

