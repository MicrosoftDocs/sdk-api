---
UID: NF:memoryapi.MapUserPhysicalPages
title: MapUserPhysicalPages function
author: windows-sdk-content
description: Maps previously allocated physical memory pages at a specified address in an Address Windowing Extensions (AWE) region.
old-location: base\mapuserphysicalpages.htm
tech.root: memory
ms.assetid: 7e9804dd-717d-4658-aac8-228878e61e4b
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MapUserPhysicalPages, MapUserPhysicalPages function, _win32_mapuserphysicalpages, base.mapuserphysicalpages, winbase/MapUserPhysicalPages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - MapUserPhysicalPages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MapUserPhysicalPages function


## -description


Maps 
    previously allocated physical memory pages at a specified address in an 
    <a href="https://msdn.microsoft.com/48a29922-8130-4540-86b0-0faa120566a6">Address Windowing Extensions</a> (AWE) region.

To perform batch mapping and unmapping of multiple regions, use the 
    <a href="https://msdn.microsoft.com/d88eaa75-38df-4498-a4c1-3dad04018c53">MapUserPhysicalPagesScatter</a> function.

<b>64-bit Windows on Itanium-based systems:  </b>Due to the difference in page sizes, 
     <b>MapUserPhysicalPages</b> is not supported for 32-bit 
     applications.


## -parameters




### -param VirtualAddress

TBD


### -param NumberOfPages [in]

The size of the physical memory and virtual address space for which to establish translations, in pages. 

The 
      virtual address range is contiguous starting at <i>lpAddress</i>. The physical frames are 
      specified by the <i>UserPfnArray</i>.

The total number of pages cannot extend from the 
      starting address beyond the end of the range that is specified in 
      <a href="https://msdn.microsoft.com/cf45b24b-0622-4ba1-b485-8429cbf146b6">AllocateUserPhysicalPages</a>.


### -param PageArray

TBD




#### - UserPfnArray [in]

A pointer to an array of physical page frame numbers. 

These frames are mapped by the argument 
      <i>lpAddress</i> on return from this function. The size of the memory that is allocated should be 
      at least the <i>NumberOfPages</i> times the size of the data type 
      <b>ULONG_PTR</b>. 
      

Do not attempt to modify this buffer. It contains operating system data, and corruption could be 
       catastrophic. The information in the buffer is not useful to an application.

If this parameter is <b>NULL</b>, the specified address range is unmapped.  Also, the specified physical pages are not 
       freed, and you must call <a href="https://msdn.microsoft.com/c01da9f1-1d24-4b7e-8c6b-50aa6f558384">FreeUserPhysicalPages</a> to 
       free them.


#### - lpAddress [in]

A pointer to the starting address of the region of memory to remap. 

The value of 
      <i>lpAddress</i> must be within the address range that the 
      <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a> function returns when the <a href="https://msdn.microsoft.com/48a29922-8130-4540-86b0-0faa120566a6">Address Windowing Extensions</a> (AWE) region is 
      allocated.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b> and no mapping is done—partial or otherwise. 
       To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The physical pages are unmapped but they are not freed. You must call 
    <a href="https://msdn.microsoft.com/c01da9f1-1d24-4b7e-8c6b-50aa6f558384">FreeUserPhysicalPages</a> to free the 
    physical pages.

Any number of physical memory pages can be specified, but the memory must  not extend outside the virtual 
    address space that <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a> allocates. Any 
    existing address maps are automatically overwritten with the new translations, and the old translations are 
    unmapped.

You cannot map physical memory pages outside the range that is specified in 
    <a href="https://msdn.microsoft.com/cf45b24b-0622-4ba1-b485-8429cbf146b6">AllocateUserPhysicalPages</a>. You 
    can map multiple regions simultaneously, but they cannot overlap.

Physical pages can be located at any physical address, but do not make assumptions about the contiguity of the 
    physical pages.

To unmap the current address range, specify <b>NULL</b> as the physical memory page array parameter. Any 
    currently mapped pages are unmapped, but are not freed. You must call 
    <a href="https://msdn.microsoft.com/c01da9f1-1d24-4b7e-8c6b-50aa6f558384">FreeUserPhysicalPages</a> to free the 
    physical pages.

In a multiprocessor environment, this function maintains hardware translation buffer coherence. On return 
    from this function, all threads on all processors are guaranteed to see the correct mapping.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more 
    information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows 
    Headers</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/1a67bd2f-afc0-48f4-91f2-34fd2b94910d">AWE Example</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/48a29922-8130-4540-86b0-0faa120566a6">Address Windowing Extensions</a>



<a href="https://msdn.microsoft.com/cf45b24b-0622-4ba1-b485-8429cbf146b6">AllocateUserPhysicalPages</a>



<a href="https://msdn.microsoft.com/c01da9f1-1d24-4b7e-8c6b-50aa6f558384">FreeUserPhysicalPages</a>



<a href="https://msdn.microsoft.com/d88eaa75-38df-4498-a4c1-3dad04018c53">MapUserPhysicalPagesScatter</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>
 

 

