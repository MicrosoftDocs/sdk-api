---
UID: NF:winddi.EngAllocPrivateUserMem
title: EngAllocPrivateUserMem macro
author: windows-sdk-content
description: The EngAllocPrivateUserMem function allocates a block of user memory from the address space of a specified process and inserts a caller-supplied tag before the allocation.
old-location: display\engallocprivateusermem.htm
old-project: display
ms.assetid: 416faebe-021b-4c00-9aba-d103a26348f6
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngAllocPrivateUserMem, EngAllocPrivateUserMem function [Display Devices], display.engallocprivateusermem, gdifncs_e31cecee-3490-46b1-ad57-4cf8c2a4f378.xml, winddi/EngAllocPrivateUserMem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngAllocPrivateUserMem
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

