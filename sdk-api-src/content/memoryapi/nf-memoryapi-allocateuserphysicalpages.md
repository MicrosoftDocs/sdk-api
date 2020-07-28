---
UID: NF:memoryapi.AllocateUserPhysicalPages
title: AllocateUserPhysicalPages function (memoryapi.h)
description: Allocates physical memory pages to be mapped and unmapped within any Address Windowing Extensions (AWE) region of a specified process.
helpviewer_keywords: ["AllocateUserPhysicalPages","AllocateUserPhysicalPages function","_win32_allocateuserphysicalpages","base.allocateuserphysicalpages","winbase/AllocateUserPhysicalPages"]
old-location: base\allocateuserphysicalpages.htm
tech.root: base
ms.assetid: cf45b24b-0622-4ba1-b485-8429cbf146b6
ms.date: 12/05/2018
ms.keywords: AllocateUserPhysicalPages, AllocateUserPhysicalPages function, _win32_allocateuserphysicalpages, base.allocateuserphysicalpages, winbase/AllocateUserPhysicalPages
f1_keywords:
- memoryapi/AllocateUserPhysicalPages
dev_langs:
- c++
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
- AllocateUserPhysicalPages
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AllocateUserPhysicalPages function


## -description


Allocates physical memory pages to be mapped and unmapped within any 
    <a href="https://docs.microsoft.com/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a> (AWE) region of 
    a specified process.

<b>64-bit Windows on Itanium-based systems:  </b>Due to the difference in page sizes, 
     <b>AllocateUserPhysicalPages</b> is not supported 
     for 32-bit applications.


## -parameters




### -param hProcess [in]

A handle to a process.

The function allocates memory that can later be mapped within the virtual address space of this process. The handle must have the <b>PROCESS_VM_OPERATION</b> access right. For more information, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>. 


### -param NumberOfPages [in, out]

The size of the physical memory to allocate, in pages.

To determine the page size of the computer, use the 
      <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function. On output, this parameter 
      receives the number of pages that are actually allocated, which might be less than the number requested.


### -param PageArray [out]

A pointer to an array to store the page frame numbers of the allocated memory.

The size of the array 
      that is allocated should be at least the <i>NumberOfPages</i> times the size of the 
      <b>ULONG_PTR</b> data type.
      

Do not attempt to modify this buffer. It contains operating system data, and corruption could be 
       catastrophic. The information in the buffer is not useful to an application.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

Fewer pages than requested can be allocated. 
      The caller must check the value of the <i>NumberOfPages</i> parameter on return to see how 
      many pages are allocated. All allocated page frame numbers are sequentially placed in the memory pointed to by 
      the <i>UserPfnArray</i> parameter.
      

If the function fails, the return value is <b>FALSE</b>, and no frames are allocated. To get extended error 
       information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The <b>AllocateUserPhysicalPages</b> function 
    is used to allocate physical memory that can later be mapped within the virtual address space of the process. The <b>SeLockMemoryPrivilege</b> privilege  must be enabled in the caller's token or the function will fail with <b>ERROR_PRIVILEGE_NOT_HELD</b>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/privilege-constants">Privilege Constants</a>.

Memory allocated by this function must be physically present in the system. 
    After the memory is allocated, it is locked down and unavailable to the rest of the virtual memory 
    management system.

Physical pages cannot be simultaneously mapped at more than one virtual address.

Physical pages can reside at any physical address. You should make no assumptions about the contiguity of the 
    physical pages.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more 
    information, see <a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/Memory/awe-example">AWE Example</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma">AllocateUserPhysicalPagesNuma</a>



<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-freeuserphysicalpages">FreeUserPhysicalPages</a>



<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-mapuserphysicalpages">MapUserPhysicalPages</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-mapuserphysicalpagesscatter">MapUserPhysicalPagesScatter</a>



<a href="https://docs.microsoft.com/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>
 

 

