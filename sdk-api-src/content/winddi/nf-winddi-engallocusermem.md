---
UID: NF:winddi.EngAllocUserMem
title: EngAllocUserMem macro (winddi.h)
description: The EngAllocUserMem function allocates a block of memory from the address space of the current process and inserts a caller-supplied tag before the allocation.
helpviewer_keywords: ["EngAllocUserMem","EngAllocUserMem function [Display Devices]","display.engallocusermem","gdifncs_fb95fed4-9948-4bc1-8917-8757ebe29442.xml","winddi/EngAllocUserMem"]
old-location: display\engallocusermem.htm
tech.root: display
ms.assetid: 5864d8dc-e239-4ba8-bd22-4a4a8952c39e
ms.date: 12/05/2018
ms.keywords: EngAllocUserMem, EngAllocUserMem function [Display Devices], display.engallocusermem, gdifncs_fb95fed4-9948-4bc1-8917-8757ebe29442.xml, winddi/EngAllocUserMem
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
 - EngAllocUserMem
 - winddi/EngAllocUserMem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngAllocUserMem
---

# EngAllocUserMem macro


## -description

The <b>EngAllocUserMem</b> function allocates a block of memory from the address space of the current process and inserts a caller-supplied tag before the allocation.

## -parameters

### -param cj [in]

Specifies the number of bytes to allocate.

### -param tag [in]

Specifies a 4-byte <a href="/windows-hardware/drivers/">pool tag</a> that uniquely identifies the driver that does the memory allocation. For more information about pool tags, see <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-exallocatepoolwithtag">ExAllocatePoolWithTag</a>.

## -remarks

A process in an NT-based operating system has 4 GB of virtual address space. The upper 2 GB is system memory that is accessible only to kernel-mode threads; this space is identical across all processes. The lower 2 GB is user memory that is accessible to both user-mode and kernel-mode threads; this space is unique to its process. The memory allocated by <b>EngAllocUserMem</b> is allocated from the unique 2 GB of user memory, and is thus accessible only when the graphics driver is called in the context of the thread in which the memory was allocated. Graphics drivers always execute in the context of the caller; that is, graphics drivers cannot switch process contexts.

<b>EngAllocUserMem</b> is particularly useful to a printer driver with large bitmaps that will only be used by the current process. Rather than allocating from the system pool, this driver can instead allocate space from the current process's address space. Drivers need to exercise care with memory allocated by <b>EngAllocUserMem</b>, as it is possible for the application to alter this memory. <b>EngAllocUserMem</b> should only be used to allocate relatively large chunks of memory, as each allocation takes at least 64 KB of virtual address space. Sensitive data structures should never be allocated using this function. Also, user memory allocated by this function cannot be passed to <a href="/windows/desktop/api/winddi/nf-winddi-engwriteprinter">EngWritePrinter</a> by the printer driver.

When the memory is no longer needed, it can be freed by a call to the <a href="/windows/desktop/api/winddi/nf-winddi-engfreeusermem">EngFreeUserMem</a> function.

To allocate user memory from the address space of a different process, use <a href="/windows/desktop/api/winddi/nf-winddi-engallocprivateusermem">EngAllocPrivateUserMem</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engallocprivateusermem">EngAllocPrivateUserMem</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engfreeusermem">EngFreeUserMem</a>