---
UID: NF:memoryapi.GetWriteWatch
title: GetWriteWatch function (memoryapi.h)
description: Retrieves the addresses of the pages that are written to in a region of virtual memory.
helpviewer_keywords: ["GetWriteWatch","GetWriteWatch function","_win32_getwritewatch","base.getwritewatch","winbase/GetWriteWatch"]
old-location: base\getwritewatch.htm
tech.root: base
ms.assetid: fa1426fe-4a1d-4300-b6f3-3e9e2272b8d3
ms.date: 12/05/2018
ms.keywords: GetWriteWatch, GetWriteWatch function, _win32_getwritewatch, base.getwritewatch, winbase/GetWriteWatch
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
 - GetWriteWatch
 - memoryapi/GetWriteWatch
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
 - GetWriteWatch
---

# GetWriteWatch function


## -description

Retrieves the addresses of 
    the pages that are written to in a region of virtual memory.

<b>64-bit Windows on Itanium-based systems:  </b>Due to the difference in page sizes, <b>GetWriteWatch</b> 
     is not supported for 32-bit applications.

## -parameters

### -param dwFlags [in]

Indicates whether the function resets the write-tracking state. 

To reset the write-tracking state, set this 
      parameter to <b>WRITE_WATCH_FLAG_RESET</b>. If this parameter is 0 (zero), 
      <b>GetWriteWatch</b> does not reset the write-tracking state. 
      For more information, see the Remarks section of this topic.

### -param lpBaseAddress [in]

The base address of the memory region for which to retrieve write-tracking information. 

This address must be in 
      a memory region that is allocated by the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> 
      function using <b>MEM_WRITE_WATCH</b>.

### -param dwRegionSize [in]

The size of the memory region for which to retrieve write-tracking information, in bytes.

### -param lpAddresses [out]

A pointer to a buffer that receives an array of page addresses in the memory region. 

The addresses indicate 
      the pages that have been written to since the region has been allocated or the write-tracking state has been reset.

### -param lpdwCount [in, out]

On input, this variable indicates the size of the <i>lpAddresses</i> array, in array 
     elements. 

On output, the variable receives the number of page addresses that are returned in the array.

### -param lpdwGranularity [out]

A pointer to a variable that receives the page size, in bytes.

## -returns

If the function succeeds, the return value is 0 (zero).

If the function fails, the return value is a nonzero value.

## -remarks

When you call the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function 
    to reserve or commit memory, you can specify <b>MEM_WRITE_WATCH</b>. This value causes the system to keep track of the 
    pages that are written to in the committed memory region. You can call the 
    <b>GetWriteWatch</b> function to retrieve the addresses of the 
    pages that have been written to since the region has been allocated or the write-tracking state has been reset.

To reset the write-tracking state, set the <b>WRITE_WATCH_FLAG_RESET</b> value in the 
    <i>dwFlags</i> parameter. Alternatively, you can call the 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch">ResetWriteWatch</a> function to reset the write-tracking 
    state. However, if you use <b>ResetWriteWatch</b>,  you must 
    ensure that no threads write to the region during the interval between the 
    <b>GetWriteWatch</b> and 
    <b>ResetWriteWatch</b> calls. Otherwise, there may be written 
    pages that you do not detect.

The <b>GetWriteWatch</b> function can be useful to 
    profilers, debugging tools, or garbage collectors.

## -see-also

<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch">ResetWriteWatch</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>