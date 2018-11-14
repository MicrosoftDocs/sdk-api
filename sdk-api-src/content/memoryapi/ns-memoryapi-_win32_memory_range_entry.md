---
UID: NS:memoryapi._WIN32_MEMORY_RANGE_ENTRY
title: "_WIN32_MEMORY_RANGE_ENTRY"
author: windows-sdk-content
description: Specifies a range of memory.
old-location: base\win32_memory_range_entry.htm
tech.root: memory
ms.assetid: d1372687-c397-4ba8-b0c0-2dcf2ec74fbb
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: "*PWIN32_MEMORY_RANGE_ENTRY, PWIN32_MEMORY_RANGE_ENTRY, PWIN32_MEMORY_RANGE_ENTRY structure pointer, WIN32_MEMORY_RANGE_ENTRY, WIN32_MEMORY_RANGE_ENTRY structure, _WIN32_MEMORY_RANGE_ENTRY, base.win32_memory_range_entry, winbase/PWIN32_MEMORY_RANGE_ENTRY, winbase/WIN32_MEMORY_RANGE_ENTRY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - WIN32_MEMORY_RANGE_ENTRY
product: Windows
targetos: Windows
req.typenames: WIN32_MEMORY_RANGE_ENTRY, *PWIN32_MEMORY_RANGE_ENTRY
req.redist: 
---

# _WIN32_MEMORY_RANGE_ENTRY structure


## -description


Specifies a range of memory. This structure is used by the 
    <a href="https://msdn.microsoft.com/a7aeeb66-afd0-4871-81a3-e4619ac84293">PrefetchVirtualMemory</a> function.


## -struct-fields




### -field VirtualAddress


### -field NumberOfBytes


## -remarks



To compile an application that calls this function, define <b>_WIN32_WINNT</b> as 
    <b>_WIN32_WINNT_WIN8</b> or higher. For more information, see 
    <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/02a2a874-9ced-4b7d-8aad-4a7768639a32">Memory Management Structures</a>



<a href="https://msdn.microsoft.com/a7aeeb66-afd0-4871-81a3-e4619ac84293">PrefetchVirtualMemory</a>
 

 

