---
UID: NF:winbase.MapUserPhysicalPagesScatter
title: MapUserPhysicalPagesScatter function (winbase.h)
description: Maps previously allocated physical memory pages at a specified address in an Address Windowing Extensions (AWE) region. (MapUserPhysicalPagesScatter)
helpviewer_keywords: ["MapUserPhysicalPagesScatter","MapUserPhysicalPagesScatter function","_win32_mapuserphysicalpagesscatter","base.mapuserphysicalpagesscatter","winbase/MapUserPhysicalPagesScatter"]
old-location: base\mapuserphysicalpagesscatter.htm
tech.root: base
ms.assetid: d88eaa75-38df-4498-a4c1-3dad04018c53
ms.date: 12/05/2018
ms.keywords: MapUserPhysicalPagesScatter, MapUserPhysicalPagesScatter function, _win32_mapuserphysicalpagesscatter, base.mapuserphysicalpagesscatter, winbase/MapUserPhysicalPagesScatter
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MapUserPhysicalPagesScatter
 - winbase/MapUserPhysicalPagesScatter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - MapUserPhysicalPagesScatter
---

# MapUserPhysicalPagesScatter function


## -description

Maps previously allocated physical memory pages at a specified address in an 
    <a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a> (AWE) region.

<b>64-bit Windows on Itanium-based systems:  </b>Due to the difference in page sizes, 
     <b>MapUserPhysicalPagesScatter</b> is not 
     supported for 32-bit applications.

## -parameters

### -param VirtualAddresses [in]

A pointer to an array of starting addresses of the regions of memory to remap. 

Each entry in 
      <i>VirtualAddresses</i> must be within the address range that the 
      <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function returns when the <a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a> (AWE) region is 
      allocated. The value in <i>NumberOfPages</i> indicates the size of the array. Entries can be from multiple Address Windowing Extensions (AWE) regions.

### -param NumberOfPages [in]

The size of the physical memory and virtual address space for which to establish translations, in pages. 

The 
      array at <i>VirtualAddresses</i> specifies the virtual address range.

### -param PageArray [in]

A pointer to an array of values that indicates how each corresponding page in 
      <i>VirtualAddresses</i> should be treated. 

A 0 (zero) indicates that the corresponding entry in 
      <i>VirtualAddresses</i> should be unmapped, and any nonzero value that it has should be mapped.
      

If this parameter is <b>NULL</b>, then every address in the <i>VirtualAddresses</i> array is 
       unmapped.

The value in <i>NumberOfPages</i> indicates the size of the array.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>, and the function does not map or unmap—partial or 
       otherwise. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The physical pages may be unmapped, but they are not freed. You must call 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-freeuserphysicalpages">FreeUserPhysicalPages</a> to free the physical 
    pages.

You can specify any number of physical memory pages, but the memory cannot extend outside the virtual 
    address space that is allocated by <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>. Any 
    existing address maps are automatically overwritten with the new translations, and the old translations are 
    unmapped.

You cannot map physical memory pages outside the range that is specified in 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpages">AllocateUserPhysicalPages</a>. You can map 
    multiple regions simultaneously, but they cannot overlap.

Physical pages can be located at any physical address, but do not make assumptions about the contiguity of the 
    physical pages.

In a multiprocessor environment, this function maintains hardware translation buffer coherence. On return 
    from this function, all threads on all processors are guaranteed to see the correct mapping.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more 
    information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows 
    Headers</a>.

## -see-also

<a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpages">AllocateUserPhysicalPages</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-freeuserphysicalpages">FreeUserPhysicalPages</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapuserphysicalpages">MapUserPhysicalPages</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>
