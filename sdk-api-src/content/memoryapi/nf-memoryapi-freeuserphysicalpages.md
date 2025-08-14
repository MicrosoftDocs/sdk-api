---
UID: NF:memoryapi.FreeUserPhysicalPages
title: FreeUserPhysicalPages function (memoryapi.h)
description: Frees physical memory pages that are allocated previously by using AllocateUserPhysicalPages or AllocateUserPhysicalPagesNuma.
helpviewer_keywords: ["FreeUserPhysicalPages","FreeUserPhysicalPages function","_win32_freeuserphysicalpages","base.freeuserphysicalpages","winbase/FreeUserPhysicalPages"]
old-location: base\freeuserphysicalpages.htm
tech.root: base
ms.assetid: c01da9f1-1d24-4b7e-8c6b-50aa6f558384
ms.date: 12/05/2018
ms.keywords: FreeUserPhysicalPages, FreeUserPhysicalPages function, _win32_freeuserphysicalpages, base.freeuserphysicalpages, winbase/FreeUserPhysicalPages
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - FreeUserPhysicalPages
 - memoryapi/FreeUserPhysicalPages
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
 - API-MS-Win-Core-memory-l1-1-2.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - FreeUserPhysicalPages
---

# FreeUserPhysicalPages function


## -description

Frees 
    physical memory pages that are allocated previously by using 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpages">AllocateUserPhysicalPages</a> or <a href="/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma">AllocateUserPhysicalPagesNuma</a>. If any of these 
    pages are currently mapped in the <a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a> (AWE) region, they are automatically unmapped by this call. This does not 
    affect the virtual address space that is occupied by a specified Address Windowing Extensions (AWE) region.

<b>64-bit Windows on Itanium-based systems:  </b>Due to the difference in page sizes, 
     <b>FreeUserPhysicalPages</b> is not supported for 
     32-bit applications.

## -parameters

### -param hProcess [in]

The handle to a process. 

The function frees memory within the virtual address space of this process.

### -param NumberOfPages [in, out]

The size of the physical memory to free, in pages. 

On return, if the function fails, this parameter indicates 
      the number of pages that are freed.

### -param PageArray [in]

A pointer to an array of page frame numbers of the allocated memory to be freed.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. In this case, the <i>NumberOfPages</i> 
       parameter reflect how many pages have actually been released. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

In a multiprocessor environment, this function maintains coherence of the hardware translation buffer. When this function returns, all threads on all processors are guaranteed to see the correct mapping.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more 
    information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows 
    Headers</a>.


#### Examples

For an example, see <a href="/windows/desktop/Memory/awe-example">AWE Example</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpages">AllocateUserPhysicalPages</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma">AllocateUserPhysicalPagesNuma</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapuserphysicalpages">MapUserPhysicalPages</a>



<a href="/windows/desktop/api/winbase/nf-winbase-mapuserphysicalpagesscatter">MapUserPhysicalPagesScatter</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>