---
UID: NF:winddi.EngAllocPrivateUserMem
title: EngAllocPrivateUserMem macro (winddi.h)
description: The EngAllocPrivateUserMem function allocates a block of user memory from the address space of a specified process and inserts a caller-supplied tag before the allocation.
helpviewer_keywords: ["EngAllocPrivateUserMem","EngAllocPrivateUserMem function [Display Devices]","display.engallocprivateusermem","gdifncs_e31cecee-3490-46b1-ad57-4cf8c2a4f378.xml","winddi/EngAllocPrivateUserMem"]
old-location: display\engallocprivateusermem.htm
tech.root: display
ms.assetid: 416faebe-021b-4c00-9aba-d103a26348f6
ms.date: 12/05/2018
ms.keywords: EngAllocPrivateUserMem, EngAllocPrivateUserMem function [Display Devices], display.engallocprivateusermem, gdifncs_e31cecee-3490-46b1-ad57-4cf8c2a4f378.xml, winddi/EngAllocPrivateUserMem
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngAllocPrivateUserMem
 - winddi/EngAllocPrivateUserMem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngAllocPrivateUserMem
---

# EngAllocPrivateUserMem macro


## -description

The <b>EngAllocPrivateUserMem</b> function allocates a block of user memory from the address space of a specified process and inserts a caller-supplied tag before the allocation.

## -parameters

### -param psl [in]

Pointer to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure representing the Microsoft DirectDraw surface with which to associate the allocated memory.

### -param cj [in]

Specifies the number of bytes of memory to allocate.

### -param tag [in]

Specifies a 4-byte <a href="/windows-hardware/drivers/">pool tag</a> that uniquely identifies the driver that does the memory allocation. For more information about pool tags, see <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-exallocatepoolwithtag">ExAllocatePoolWithTag</a>.

## -remarks

A DirectDraw driver might require a user-memory "scratch pad" in place of true video memory. Although this practice is discouraged due to its performance implications, it is occasionally necessary. This scratch memory is usually allocated only for a short period of time. After the memory has been allocated, it is used for the intended graphics operations, and then deallocated.

A problem arises if the driver instance is destroyed before the surface is unlocked. A particular case occurs when the system switches to a protected desktop as a result of a user pressing CTRL+ALT+DEL. In this situation, the mode switch is performed on a system process context. If the driver has any outstanding surface locks, such as when the mode switch happens before the surface has been unlocked, the driver will be required to destroy that surface on a different process context. The driver cannot call <a href="/windows/desktop/api/winddi/nf-winddi-engfreeusermem">EngFreeUserMem</a> to deallocate the scratch memory since this entry point will fail if called on a different context from that used when the memory was allocated.

<b>EngAllocPrivateUserMem</b>, and <a href="/windows/desktop/api/winddi/nf-winddi-engfreeprivateusermem">EngFreePrivateUserMem</a> are provided to address this problem. These two functions are identical to <a href="/windows/desktop/api/winddi/nf-winddi-engallocusermem">EngAllocUserMem</a> and <a href="/windows/desktop/api/winddi/nf-winddi-engfreeusermem">EngFreeUserMem</a>, except that they do the extra work required to free memory allocated on a different process context. Process context information is stored with the DirectDraw object that owns the DirectDraw surface object to which <i>psl</i> points.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_global">DD_SURFACE_GLOBAL</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engallocusermem">EngAllocUserMem</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engfreeprivateusermem">EngFreePrivateUserMem</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engfreeusermem">EngFreeUserMem</a>