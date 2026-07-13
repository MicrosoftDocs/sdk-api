---
UID: NF:memoryapi.VirtualFreeEx
title: VirtualFreeEx function (memoryapi.h)
description: Releases, decommits, or releases and decommits a region of memory within the virtual address space of a specified process.
helpviewer_keywords: ["MEM_COALESCE_PLACEHOLDERS","MEM_DECOMMIT","MEM_PRESERVE_PLACEHOLDER","MEM_RELEASE","VirtualFreeEx","VirtualFreeEx function","_win32_virtualfreeex","base.virtualfreeex","winbase/VirtualFreeEx"]
old-location: base\virtualfreeex.htm
tech.root: base
ms.assetid: 2e5c862c-1251-49da-9c3a-90b09e488d89
ms.date: 5/18/2022
ms.keywords: MEM_COALESCE_PLACEHOLDERS, MEM_DECOMMIT, MEM_PRESERVE_PLACEHOLDER, MEM_RELEASE, VirtualFreeEx, VirtualFreeEx function, _win32_virtualfreeex, base.virtualfreeex, winbase/VirtualFreeEx
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
 - VirtualFreeEx
 - memoryapi/VirtualFreeEx
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
 - API-MS-Win-Core-memory-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - VirtualFreeEx
---

# VirtualFreeEx function


## -description

Releases, decommits, or releases and decommits a region of memory within the virtual address space of a specified process.

## -parameters

### -param hProcess [in]

A handle to a process. The function frees memory within the virtual address space of the process.

The handle must have the <b>PROCESS_VM_OPERATION</b> access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param lpAddress [in]

A pointer to the starting address of the region of memory to be freed. 

If the <i>dwFreeType</i> parameter is <b>MEM_RELEASE</b>, <i>lpAddress</i> must be the base address returned by the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a> function when the region is reserved.

### -param dwSize [in]

The size of the region of memory to free, in bytes. 




If the <i>dwFreeType</i> parameter is <b>MEM_RELEASE</b>, <i>dwSize</i> must be 0 (zero). The function frees the entire region that is reserved in the initial allocation call to 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a>.

If <i>dwFreeType</i> is <b>MEM_DECOMMIT</b>, the function decommits all memory pages that contain one or more bytes in the range from the <i>lpAddress</i> parameter to <code>(lpAddress+dwSize)</code>. This means, for example, that a 2-byte region of memory that straddles a page boundary causes both pages to be decommitted. If <i>lpAddress</i> is the base address returned by 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a> and <i>dwSize</i> is 0 (zero), the function decommits the entire region that is allocated by 
<b>VirtualAllocEx</b>. After that, the entire region is in the reserved state.

### -param dwFreeType [in]

The type of free operation. This parameter must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEM_DECOMMIT"></a><a id="mem_decommit"></a><dl>
<dt><b>MEM_DECOMMIT</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Decommits the specified region of committed pages. After the operation, the pages are in the reserved state.

The function does not fail if you attempt to decommit an uncommitted page. This means that you can decommit a range of pages without first determining the current commitment state.

The <b>MEM_DECOMMIT</b> value is not supported when the <i>lpAddress</i> parameter provides the base address for an enclave. This is true for enclaves that do not support dynamic memory management (i.e. SGX1). SGX2 enclaves permit MEM_DECOMMIT anywhere in the enclave.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_RELEASE"></a><a id="mem_release"></a><dl>
<dt><b>MEM_RELEASE</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Releases the specified region of pages, or placeholder (for a placeholder, the address space is released and available for other allocations). After this operation, the pages are in the free state. 


If you specify this value, <i>dwSize</i> must be 0 (zero), and <i>lpAddress</i> must point to the base address returned by the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function when the region is reserved. The function fails if either of these conditions is not met.

If any pages in the region are committed currently, the function first decommits, and then releases them.

The function does not fail if you attempt to release pages that are in different states, some reserved and some committed. This means that you can release a range of pages without first determining the current commitment state.

</td>
</tr>
</table>


When using <b>MEM_RELEASE</b>, this parameter can additionally specify one of the following values.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEM_COALESCE_PLACEHOLDERS"></a><a id="mem_coalesce_placeholders"></a><dl>
<dt><b>MEM_COALESCE_PLACEHOLDERS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
To coalesce two adjacent placeholders, specify <code>MEM_RELEASE | MEM_COALESCE_PLACEHOLDERS</code>. When you coalesce placeholders, <i>lpAddress</i> and <i>dwSize</i> must exactly match the overall range of the placeholders to be merged.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_PRESERVE_PLACEHOLDER"></a><a id="mem_preserve_placeholder"></a><dl>
<dt><b>MEM_PRESERVE_PLACEHOLDER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Frees an allocation back to a placeholder (after you've replaced a placeholder with a private allocation using <a href="../memoryapi/nf-memoryapi-virtualalloc2.md">VirtualAlloc2</a> or <a href="https://msdn.microsoft.com/en-us/library/Mt832850(v=VS.85).aspx">Virtual2AllocFromApp</a>).

To split a placeholder into two placeholders, specify <code>MEM_RELEASE | MEM_PRESERVE_PLACEHOLDER</code>.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Each page of memory in a process virtual address space has a 
<a href="/windows/desktop/Memory/page-state">Page State</a>.  The 
<b>VirtualFreeEx</b> function can decommit a range of pages that are in different states, some committed and some uncommitted. This means that you can decommit a range of pages without first determining the current commitment state of each page. Decommitting a page releases its physical storage, either in memory or in the paging file on disk.

If a page is decommitted but not released, its state changes to reserved. Subsequently, you can  call 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a> to commit it, or 
<b>VirtualFreeEx</b> to release it. Attempting to read from or write to a reserved page results in an access violation exception.

The **VirtualFreeEx** function can release a range of pages that are in different states, some reserved and some committed. This means that you can release a range of pages without first determining the current commitment state of each page. The entire range of pages originally reserved by [VirtualAllocEx](nf-memoryapi-virtualallocex.md) must be released at the same time.

If a page is released, its state changes to free, and it is available for subsequent allocation operations. After memory is released or decommitted, you can never refer to the memory again. Any information that may have been in that memory is gone forever. Attempts to read from or write to a free page results in an access violation exception. If you need to keep information, do not decommit or free memory that  contains the information.

The **VirtualFreeEx** function can be used on an AWE region of memory and it invalidates any physical page mappings in the region when freeing the address space. However, the physical pages are not deleted, and the application can use them. The application must explicitly call [FreeUserPhysicalPages](nf-memoryapi-freeuserphysicalpages.md) to free the physical pages. When the  process is terminated, all resources are automatically cleaned up.

**Windows 10, version 1709 and later and Windows 11:** To delete the enclave when you finish using it, call [DeleteEnclave](../enclaveapi/nf-enclaveapi-deleteenclave.md). You cannot delete a VBS enclave by calling the [VirtualFree](nf-memoryapi-virtualfree.md) or **VirtualFreeEx** function. You can still delete an SGX enclave by calling **VirtualFree** or **VirtualFreeEx**.

**Windows 10, version 1507, Windows 10, version 1511, Windows 10, version 1607 and Windows 10, version 1703:** To delete the enclave when you finish using it, call the [VirtualFree](nf-memoryapi-virtualfree.md) or **VirtualFreeEx** function and specify the following values:

- The base address of the enclave for the _lpAddress_ parameter.
- 0 for the _dwSize_ parameter.
- **MEM_RELEASE** for the _dwFreeType_ parameter.

## -see-also

[Memory Management Functions](/windows/win32/Memory/memory-management-functions)

[Virtual Memory Functions](/windows/win32/Memory/virtual-memory-functions)

[VirtualAllocEx](nf-memoryapi-virtualallocex.md)
