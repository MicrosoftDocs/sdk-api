---
UID: NF:memoryapi.ResetWriteWatch
title: ResetWriteWatch function (memoryapi.h)
description: Resets the write-tracking state for a region of virtual memory. Subsequent calls to the GetWriteWatch function only report pages that are written to since the reset operation.
helpviewer_keywords: ["ResetWriteWatch","ResetWriteWatch function","_win32_resetwritewatch","base.resetwritewatch","winbase/ResetWriteWatch"]
old-location: base\resetwritewatch.htm
tech.root: base
ms.assetid: afbc5a58-01e2-4f32-bc47-351fe846e4a5
ms.date: 12/05/2018
ms.keywords: ResetWriteWatch, ResetWriteWatch function, _win32_resetwritewatch, base.resetwritewatch, winbase/ResetWriteWatch
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResetWriteWatch
 - memoryapi/ResetWriteWatch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - ResetWriteWatch
---

# ResetWriteWatch function


## -description

Resets the 
    write-tracking state for a region of virtual memory. Subsequent calls to the 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch">GetWriteWatch</a> function only report pages that are written to since the reset operation.

<b>64-bit Windows on Itanium-based systems:  </b>Due to the difference in page sizes, <b>ResetWriteWatch</b> 
     is not supported for 32-bit applications.

## -parameters

### -param lpBaseAddress [in]

A pointer to the base address of the memory region for which to reset the write-tracking state. 

This address 
      must be in a memory region that is allocated by the 
      <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function with <b>MEM_WRITE_WATCH</b>.

### -param dwRegionSize [in]

The size of the memory region for which to reset the write-tracking information, in bytes.

## -returns

If the function succeeds, the return value is 0 (zero).

If the function fails, the return value is a nonzero value.

## -remarks

The <b>ResetWriteWatch</b> function can be useful to an 
    application such as a garbage collector. The application calls the 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch">GetWriteWatch</a> function to retrieve the list of written 
    pages, and then writes to those pages as part of its cleanup operation. Then the garbage collector calls 
    <b>ResetWriteWatch</b> to remove the write-tracking records 
    caused by the cleanup.

You can also reset the write-tracking state of a memory region by specifying <b>WRITE_WATCH_FLAG_RESET</b> when you 
    call <a href="/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch">GetWriteWatch</a>.

If you use <b>ResetWriteWatch</b>, you must ensure that 
    no threads write to the region during the interval between the 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch">GetWriteWatch</a> and 
    <b>ResetWriteWatch</b> calls. Otherwise, there may be written 
    pages that you not detect.

## -see-also

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch">GetWriteWatch</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>