---
UID: NF:winddi.EngAllocMem
title: EngAllocMem macro (winddi.h)
description: The EngAllocMem function allocates a block of memory and inserts a caller-supplied tag before the allocation.
old-location: display\engallocmem.htm
tech.root: display
ms.assetid: 61bef5a1-bf68-4d37-ae5d-13ff045a2344
ms.date: 12/05/2018
ms.keywords: EngAllocMem, EngAllocMem function [Display Devices], display.engallocmem, gdifncs_c8084f74-b624-4f79-be0a-cf1fc144afaa.xml, winddi/EngAllocMem
ms.topic: macro
f1_keywords:
- winddi/EngAllocMem
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Win32k.sys
api_name:
- EngAllocMem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngAllocMem macro


## -description


The <b>EngAllocMem</b> function allocates a block of memory and inserts a caller-supplied tag before the allocation.


## -parameters




### -param flags [in]

Specifies how to allocate memory. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FL_NONPAGED_MEMORY

</td>
<td>
Allocate memory from the nonpaged pool. If this flag is not set, the memory is allocated from the system's paged pool.

</td>
</tr>
<tr>
<td>
FL_ZERO_MEMORY

</td>
<td>
Zero-initialize the allocated memory. If this flag is not set, the memory is returned uninitialized.

</td>
</tr>
</table>
 


### -param cj [in]

Specifies the number of bytes to allocate.


### -param tag [in]

Specifies a 4-byte <a href="https://docs.microsoft.com/windows-hardware/drivers/">pool tag</a> that uniquely identifies the driver that does the memory allocation. For more information about pool tags, see <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-exallocatepoolwithtag">ExAllocatePoolWithTag</a>.


## -remarks



When the memory is no longer needed, it should be freed by a call to the <b>EngFreeMem</b> function. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engfreemem">EngFreeMem</a>
 

 

