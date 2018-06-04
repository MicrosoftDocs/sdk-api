---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# MapUserPhysicalPagesScatter function


## -description


Maps previously allocated physical memory pages at a specified address in an 
    <a href="https://msdn.microsoft.com/48a29922-8130-4540-86b0-0faa120566a6">Address Windowing Extensions</a> (AWE) region.

<b>64-bit Windows on Itanium-based systems:  </b>Due to the difference in page sizes, 
     <b>MapUserPhysicalPagesScatter</b> is not 
     supported for 32-bit applications.


## -parameters




### -param VirtualAddresses [in]

A pointer to an array of starting addresses of the regions of memory to remap. 

Each entry in 
      <i>VirtualAddresses</i> must be within the address range that the 
      <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a> function returns when the <a href="https://msdn.microsoft.com/48a29922-8130-4540-86b0-0faa120566a6">Address Windowing Extensions</a> (AWE) region is 
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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The physical pages may be unmapped, but they are not freed. You must call 
    <a href="https://msdn.microsoft.com/c01da9f1-1d24-4b7e-8c6b-50aa6f558384">FreeUserPhysicalPages</a> to free the physical 
    pages.

You can specify any number of physical memory pages, but the memory cannot extend outside the virtual 
    address space that is allocated by <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>. Any 
    existing address maps are automatically overwritten with the new translations, and the old translations are 
    unmapped.

You cannot map physical memory pages outside the range that is specified in 
    <a href="https://msdn.microsoft.com/cf45b24b-0622-4ba1-b485-8429cbf146b6">AllocateUserPhysicalPages</a>. You can map 
    multiple regions simultaneously, but they cannot overlap.

Physical pages can be located at any physical address, but do not make assumptions about the contiguity of the 
    physical pages.

In a multiprocessor environment, this function maintains hardware translation buffer coherence. On return 
    from this function, all threads on all processors are guaranteed to see the correct mapping.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more 
    information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows 
    Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/48a29922-8130-4540-86b0-0faa120566a6">Address Windowing Extensions</a>



<a href="https://msdn.microsoft.com/cf45b24b-0622-4ba1-b485-8429cbf146b6">AllocateUserPhysicalPages</a>



<a href="https://msdn.microsoft.com/c01da9f1-1d24-4b7e-8c6b-50aa6f558384">FreeUserPhysicalPages</a>



<a href="https://msdn.microsoft.com/7e9804dd-717d-4658-aac8-228878e61e4b">MapUserPhysicalPages</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>
 

 

