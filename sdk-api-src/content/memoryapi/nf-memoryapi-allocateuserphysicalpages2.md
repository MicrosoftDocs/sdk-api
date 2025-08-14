---
UID: NF:memoryapi.AllocateUserPhysicalPages2
tech.root: base
title: AllocateUserPhysicalPages2
ms.date: 12/07/2023
targetos: Windows
description: Allocates physical memory pages to be mapped and unmapped within any Address Windowing Extensions (AWE) region of a specified process, with extended parameters.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: kernelbase.dll
req.header: memoryapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: onecore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, Build 20348
req.target-min-winversvr: Windows Server, Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - kernelbase.dll
api_name:
 - AllocateUserPhysicalPages2
f1_keywords:
 - AllocateUserPhysicalPages2
 - memoryapi/AllocateUserPhysicalPages2
dev_langs:
 - c++
helpviewer_keywords:
 - AllocateUserPhysicalPages2
---

# AllocateUserPhysicalPages2 function

## -description

Allocates physical memory pages to be mapped and unmapped within any [Address Windowing Extensions (AWE)](/windows/desktop/Memory/address-windowing-extensions) region of a specified process, with extended parameters.

## -parameters

### -param ObjectHandle [in]

A handle to a process.

The function allocates memory that can later be mapped within the virtual address space of this process. The handle must have the <b>PROCESS_VM_OPERATION</b> access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param NumberOfPages [in,out]

The size of the physical memory to allocate, in pages.

To determine the page size of the computer, use the [GetSystemInfo](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function. On output, this parameter receives the number of pages that are actually allocated, which might be less than the number requested.

### -param PageArray [out]

A pointer to an array to store the page frame numbers of the allocated memory.

The size of the array that is allocated should be at least the *NumberOfPages* times the size of the **ULONG_PTR** data type.

Do not attempt to modify this buffer. It contains operating system data, and corruption could be catastrophic. The information in the buffer is not useful to an application.

### -param ExtendedParameters [in,out]

Pointer to an array of [MEM_EXTENDED_PARAMETER](/windows/win32/api/winnt/ns-winnt-mem_extended_parameter) structures.

### -param ExtendedParameterCount [in]

The number of **MEM_EXTENDED_PARAMETER** in the *ExtendedParameters* array.

## -returns

If the function succeeds, the return value is **TRUE**.

Fewer pages than requested can be allocated. The caller must check the value of the *NumberOfPages* parameter on return to see how many pages are allocated. All allocated page frame numbers are sequentially placed in the memory pointed to by the *UserPfnArray* parameter.

If the function fails, the return value is **FALSE**, and no frames are allocated. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

**AllocateUserPhysicalPages2** is the same as [AllocateUserPhysicalPages](nf-memoryapi-allocateuserphysicalpages.md) but it adds the *ExtendedParameters* and *ExtendedParameterCount* parameters.


The **AllocateUserPhysicalPages2** function is used to allocate physical memory that can later be mapped within the virtual address space of the process. The **SeLockMemoryPrivilege** privilege  must be enabled in the caller's token or the function will fail with **ERROR_PRIVILEGE_NOT_HELD**. For more information, see [Privilege Constants](/windows/desktop/SecAuthZ/privilege-constants).

Memory allocated by this function must be physically present in the system. After the memory is allocated, it is locked down and unavailable to the rest of the virtual memory management system.

Physical pages cannot be simultaneously mapped at more than one virtual address.

Physical pages can reside at any physical address. You should make no assumptions about the contiguity of the physical pages.

## -see-also

[AllocateUserPhysicalPages](nf-memoryapi-allocateuserphysicalpages.md)

<a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma">AllocateUserPhysicalPagesNuma</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-freeuserphysicalpages">FreeUserPhysicalPages</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapuserphysicalpages">MapUserPhysicalPages</a>



<a href="/windows/desktop/api/winbase/nf-winbase-mapuserphysicalpagesscatter">MapUserPhysicalPagesScatter</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>
