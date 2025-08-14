---
UID: NF:memoryapi.MapUserPhysicalPages
title: MapUserPhysicalPages function (memoryapi.h)
description: Maps previously allocated physical memory pages at a specified address in an Address Windowing Extensions (AWE) region. (MapUserPhysicalPages)
helpviewer_keywords: ["MapUserPhysicalPages","MapUserPhysicalPages function","_win32_mapuserphysicalpages","base.mapuserphysicalpages","winbase/MapUserPhysicalPages"]
old-location: base\mapuserphysicalpages.htm
tech.root: base
ms.assetid: 7e9804dd-717d-4658-aac8-228878e61e4b
ms.date: 12/05/2018
ms.keywords: MapUserPhysicalPages, MapUserPhysicalPages function, _win32_mapuserphysicalpages, base.mapuserphysicalpages, winbase/MapUserPhysicalPages
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
 - MapUserPhysicalPages
 - memoryapi/MapUserPhysicalPages
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
 - MapUserPhysicalPages
---

# MapUserPhysicalPages function


## -description

Maps 
    previously allocated physical memory pages at a specified address in an 
    <a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a> (AWE) region.

To perform batch mapping and unmapping of multiple regions, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-mapuserphysicalpagesscatter">MapUserPhysicalPagesScatter</a> function.

<b>64-bit Windows on Itanium-based systems:  </b>Due to the difference in page sizes, 
     <b>MapUserPhysicalPages</b> is not supported for 32-bit 
     applications.

## -parameters

### -param VirtualAddress [in]

A pointer to the starting address of the region of memory to remap. 

The value of 
      <i>lpAddress</i> must be within the address range that the 
      <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function returns when the <a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a> (AWE) region is 
      allocated.

### -param NumberOfPages [in]

The size of the physical memory and virtual address space for which to establish translations, in pages. 

The 
      virtual address range is contiguous starting at <i>lpAddress</i>. The physical frames are 
      specified by the <i>UserPfnArray</i>.

The total number of pages cannot extend from the 
      starting address beyond the end of the range that is specified in 
      <a href="/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpages">AllocateUserPhysicalPages</a>.

### -param PageArray [in]

A pointer to an array of physical page frame numbers. 

These frames are mapped by the argument 
      <i>lpAddress</i> on return from this function. The size of the memory that is allocated should be 
      at least the <i>NumberOfPages</i> times the size of the data type 
      <b>ULONG_PTR</b>. 
      

Do not attempt to modify this buffer. It contains operating system data, and corruption could be 
       catastrophic. The information in the buffer is not useful to an application.

If this parameter is <b>NULL</b>, the specified address range is unmapped.  Also, the specified physical pages are not 
       freed, and you must call <a href="/windows/desktop/api/memoryapi/nf-memoryapi-freeuserphysicalpages">FreeUserPhysicalPages</a> to 
       free them.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b> and no mapping is done—partial or otherwise. 
       To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The physical pages are unmapped but they are not freed. You must call 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-freeuserphysicalpages">FreeUserPhysicalPages</a> to free the 
    physical pages.

Any number of physical memory pages can be specified, but the memory must  not extend outside the virtual 
    address space that <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> allocates. Any 
    existing address maps are automatically overwritten with the new translations, and the old translations are 
    unmapped.

You cannot map physical memory pages outside the range that is specified in 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpages">AllocateUserPhysicalPages</a>. You 
    can map multiple regions simultaneously, but they cannot overlap.

Physical pages can be located at any physical address, but do not make assumptions about the contiguity of the 
    physical pages.

To unmap the current address range, specify <b>NULL</b> as the physical memory page array parameter. Any 
    currently mapped pages are unmapped, but are not freed. You must call 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-freeuserphysicalpages">FreeUserPhysicalPages</a> to free the 
    physical pages.

In a multiprocessor environment, this function maintains hardware translation buffer coherence. On return 
    from this function, all threads on all processors are guaranteed to see the correct mapping.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more 
    information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows 
    Headers</a>.


#### Examples

For an example, see <a href="/windows/desktop/Memory/awe-example">AWE Example</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpages">AllocateUserPhysicalPages</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-freeuserphysicalpages">FreeUserPhysicalPages</a>



<a href="/windows/desktop/api/winbase/nf-winbase-mapuserphysicalpagesscatter">MapUserPhysicalPagesScatter</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>
