---
UID: NF:memoryapi.AllocateUserPhysicalPagesNuma
title: AllocateUserPhysicalPagesNuma function (memoryapi.h)
description: Allocates physical memory pages to be mapped and unmapped within any Address Windowing Extensions (AWE) region of a specified process and specifies the NUMA node for the physical memory.
helpviewer_keywords: ["AllocateUserPhysicalPagesNuma","AllocateUserPhysicalPagesNuma function","base.allocateuserphysicalpagesnuma","winbase/AllocateUserPhysicalPagesNuma"]
old-location: base\allocateuserphysicalpagesnuma.htm
tech.root: base
ms.assetid: 33af02c8-609f-4490-b17e-e116d24c217c
ms.date: 12/05/2018
ms.keywords: AllocateUserPhysicalPagesNuma, AllocateUserPhysicalPagesNuma function, base.allocateuserphysicalpagesnuma, winbase/AllocateUserPhysicalPagesNuma
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - AllocateUserPhysicalPagesNuma
 - memoryapi/AllocateUserPhysicalPagesNuma
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
 - AllocateUserPhysicalPagesNuma
---

# AllocateUserPhysicalPagesNuma function


## -description

Allocates physical memory pages to be mapped and unmapped within any 
    <a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a> (AWE) region of a 
    specified process  and specifies the NUMA node for the physical memory.

## -parameters

### -param hProcess [in]

A handle to a process. 

The function allocates memory that can later be mapped within the virtual address 
      space of this process. The handle must have the <b>PROCESS_VM_OPERATION</b> access right. For 
      more information, see 
      <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param NumberOfPages [in, out]

The size of the physical memory to allocate, in pages.

To determine the page size of the computer, use the 
       <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function. On output, this parameter 
       receives the number of pages that are actually allocated, which might be less than the number requested.

### -param PageArray [out]

A pointer to an array to store the page frame numbers of the allocated memory.

The size of the array that is allocated should be at least the <i>NumberOfPages</i> times 
       the size of the <b>ULONG_PTR</b> data type.

<div class="alert"><b>Caution</b>  Do not attempt to modify this buffer. It contains operating system data, and corruption 
       could be catastrophic. The information in the buffer is not useful to an application.</div>
<div> </div>

### -param nndPreferred [in]

The NUMA node where the physical memory should reside.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

Fewer pages than requested can be allocated. The caller must check the value of the 
       <i>NumberOfPages</i> parameter on return to see how many pages are allocated. All allocated 
       page frame numbers are sequentially placed in the memory pointed to by the <i>PageArray</i> 
       parameter.

If the function fails, the return value is <b>FALSE</b> and no frames are allocated. To get 
       extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> 
       function.

## -remarks

The <b>AllocateUserPhysicalPagesNuma</b> 
    function is used to allocate physical memory within a NUMA node that can later be mapped within the virtual 
    address space of the process. The <b>SeLockMemoryPrivilege</b> privilege must be enabled in the 
    caller's token or the function will fail with <b>ERROR_PRIVILEGE_NOT_HELD</b>. For more 
    information, see <a href="/windows/desktop/SecAuthZ/privilege-constants">Privilege Constants</a>.

Memory allocated by this function must be physically present in the system. After the memory is allocated, it 
    is locked down and unavailable to the rest of the virtual memory management system.

Physical pages cannot be simultaneously mapped at more than one virtual address.

Physical pages can reside at any physical address. You should make no assumptions about the contiguity of the 
    physical pages.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 
    or later.

## -see-also

<a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpages">AllocateUserPhysicalPages</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-freeuserphysicalpages">FreeUserPhysicalPages</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>