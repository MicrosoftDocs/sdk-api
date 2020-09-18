---
UID: NS:memoryapi._WIN32_MEMORY_RANGE_ENTRY
title: WIN32_MEMORY_RANGE_ENTRY (memoryapi.h)
description: Specifies a range of memory.
helpviewer_keywords: ["*PWIN32_MEMORY_RANGE_ENTRY","PWIN32_MEMORY_RANGE_ENTRY","PWIN32_MEMORY_RANGE_ENTRY structure pointer","WIN32_MEMORY_RANGE_ENTRY","WIN32_MEMORY_RANGE_ENTRY structure","_WIN32_MEMORY_RANGE_ENTRY","base.win32_memory_range_entry","winbase/PWIN32_MEMORY_RANGE_ENTRY","winbase/WIN32_MEMORY_RANGE_ENTRY"]
old-location: base\win32_memory_range_entry.htm
tech.root: base
ms.assetid: d1372687-c397-4ba8-b0c0-2dcf2ec74fbb
ms.date: 12/05/2018
ms.keywords: '*PWIN32_MEMORY_RANGE_ENTRY, PWIN32_MEMORY_RANGE_ENTRY, PWIN32_MEMORY_RANGE_ENTRY structure pointer, WIN32_MEMORY_RANGE_ENTRY, WIN32_MEMORY_RANGE_ENTRY structure, _WIN32_MEMORY_RANGE_ENTRY, base.win32_memory_range_entry, winbase/PWIN32_MEMORY_RANGE_ENTRY, winbase/WIN32_MEMORY_RANGE_ENTRY'
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
targetos: Windows
req.typenames: WIN32_MEMORY_RANGE_ENTRY, *PWIN32_MEMORY_RANGE_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WIN32_MEMORY_RANGE_ENTRY
 - memoryapi/_WIN32_MEMORY_RANGE_ENTRY
 - PWIN32_MEMORY_RANGE_ENTRY
 - memoryapi/PWIN32_MEMORY_RANGE_ENTRY
 - WIN32_MEMORY_RANGE_ENTRY
 - memoryapi/WIN32_MEMORY_RANGE_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - WIN32_MEMORY_RANGE_ENTRY
---

# WIN32_MEMORY_RANGE_ENTRY structure


## -description

Specifies a range of memory. This structure is used by the 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-prefetchvirtualmemory">PrefetchVirtualMemory</a> function.

## -struct-fields

### -field VirtualAddress

### -field NumberOfBytes

## -remarks

To compile an application that calls this function, define <b>_WIN32_WINNT</b> as 
    <b>_WIN32_WINNT_WIN8</b> or higher. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/Memory/memory-management-structures">Memory Management Structures</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-prefetchvirtualmemory">PrefetchVirtualMemory</a>