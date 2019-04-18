---
UID: NF:memoryapi.FreeUserPhysicalPages
title: FreeUserPhysicalPages function (memoryapi.h)
author: windows-sdk-content
description: Frees physical memory pages that are allocated previously by using AllocateUserPhysicalPages or AllocateUserPhysicalPagesNuma.
old-location: base\freeuserphysicalpages.htm
tech.root: Memory
ms.assetid: c01da9f1-1d24-4b7e-8c6b-50aa6f558384
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FreeUserPhysicalPages, FreeUserPhysicalPages function, _win32_freeuserphysicalpages, base.freeuserphysicalpages, winbase/FreeUserPhysicalPages
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
 - FreeUserPhysicalPages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FreeUserPhysicalPages function


## -description


Frees 
    physical memory pages that are allocated previously by using 
    <a href="https://msdn.microsoft.com/cf45b24b-0622-4ba1-b485-8429cbf146b6">AllocateUserPhysicalPages</a> or <a href="https://msdn.microsoft.com/33af02c8-609f-4490-b17e-e116d24c217c">AllocateUserPhysicalPagesNuma</a>. If any of these 
    pages are currently mapped in the <a href="https://msdn.microsoft.com/48a29922-8130-4540-86b0-0faa120566a6">Address Windowing Extensions</a> (AWE) region, they are automatically unmapped by this call. This does not 
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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



In a multiprocessor environment, this function maintains coherence of the hardware translation buffer. When this function returns, all threads on all processors are guaranteed to see the correct mapping.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more 
    information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows 
    Headers</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/1a67bd2f-afc0-48f4-91f2-34fd2b94910d">AWE Example</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/48a29922-8130-4540-86b0-0faa120566a6">Address Windowing Extensions</a>



<a href="https://msdn.microsoft.com/cf45b24b-0622-4ba1-b485-8429cbf146b6">AllocateUserPhysicalPages</a>



<a href="https://msdn.microsoft.com/33af02c8-609f-4490-b17e-e116d24c217c">AllocateUserPhysicalPagesNuma</a>



<a href="https://msdn.microsoft.com/7e9804dd-717d-4658-aac8-228878e61e4b">MapUserPhysicalPages</a>



<a href="https://msdn.microsoft.com/d88eaa75-38df-4498-a4c1-3dad04018c53">MapUserPhysicalPagesScatter</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>
 

 

