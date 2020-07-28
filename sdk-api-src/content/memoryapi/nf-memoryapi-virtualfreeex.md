---
UID: NF:memoryapi.VirtualFreeEx
title: VirtualFreeEx function (memoryapi.h)
description: Releases, decommits, or releases and decommits a region of memory within the virtual address space of a specified process.
helpviewer_keywords: ["MEM_COALESCE_PLACEHOLDERS","MEM_DECOMMIT","MEM_PRESERVE_PLACEHOLDER","MEM_RELEASE","VirtualFreeEx","VirtualFreeEx function","_win32_virtualfreeex","base.virtualfreeex","winbase/VirtualFreeEx"]
old-location: base\virtualfreeex.htm
tech.root: base
ms.assetid: 2e5c862c-1251-49da-9c3a-90b09e488d89
ms.date: 12/05/2018
ms.keywords: MEM_COALESCE_PLACEHOLDERS, MEM_DECOMMIT, MEM_PRESERVE_PLACEHOLDER, MEM_RELEASE, VirtualFreeEx, VirtualFreeEx function, _win32_virtualfreeex, base.virtualfreeex, winbase/VirtualFreeEx
f1_keywords:
- memoryapi/VirtualFreeEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VirtualFreeEx function


## -description


Releases, decommits, or releases and decommits a region of memory within the virtual address space of a specified process.


## -parameters




### -param hProcess [in]

A handle to a process. The function frees memory within the virtual address space of the process. 




The handle must have the <b>PROCESS_VM_OPERATION</b> access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.


### -param lpAddress [in]

A pointer to the starting address of the region of memory to be freed. 




If the <i>dwFreeType</i> parameter is <b>MEM_RELEASE</b>, <i>lpAddress</i> must be the base address returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a> function when the region is reserved.


### -param dwSize [in]

The size of the region of memory to free, in bytes. 




If the <i>dwFreeType</i> parameter is <b>MEM_RELEASE</b>, <i>dwSize</i> must be 0 (zero). The function frees the entire region that is reserved in the initial allocation call to 
<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a>.

If <i>dwFreeType</i> is <b>MEM_DECOMMIT</b>, the function decommits all memory pages that contain one or more bytes in the range from the <i>lpAddress</i> parameter to <code>(lpAddress+dwSize)</code>. This means, for example, that a 2-byte region of memory that straddles a page boundary causes both pages to be decommitted. If <i>lpAddress</i> is the base address returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a> and <i>dwSize</i> is 0 (zero), the function decommits the entire region that is allocated by 
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

The <b>MEM_DECOMMIT</b> value is not supported when the <i>lpAddress</i> parameter provides the base address for an enclave.

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
<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function when the region is reserved. The function fails if either of these conditions is not met.

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
To coalesce two adjacent placeholders, specify <code>MEM_RELEASE | MEM_COALESCE_PLACEHOLDERS</code>. When you coalesce placeholders, <i>lpAddress</i> and <i>dwSize</i> must exactly match those of the placeholder.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_PRESERVE_PLACEHOLDER"></a><a id="mem_preserve_placeholder"></a><dl>
<dt><b>MEM_PRESERVE_PLACEHOLDER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Frees an allocation back to a placeholder (after you've replaced a placeholder with a private allocation using <a href="https://msdn.microsoft.com/en-us/library/Mt832849(v=VS.85).aspx">VirtualAlloc2</a> or <a href="https://msdn.microsoft.com/en-us/library/Mt832850(v=VS.85).aspx">Virtual2AllocFromApp</a>).

To split a placeholder into two placeholders, specify <code>MEM_RELEASE | MEM_PRESERVE_PLACEHOLDER</code>.

</td>
</tr>
</table>

## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Each page of memory in a process virtual address space has a 
<a href="https://docs.microsoft.com/windows/desktop/Memory/page-state">Page State</a>.  The 
<b>VirtualFreeEx</b> function can decommit a range of pages that are in different states, some committed and some uncommitted. This means that you can decommit a range of pages without first determining the current commitment state of each page. Decommitting a page releases its physical storage, either in memory or in the paging file on disk.

If a page is decommitted but not released, its state changes to reserved. Subsequently, you can  call 
<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a> to commit it, or 
<b>VirtualFreeEx</b> to release it. Attempting to read from or write to a reserved page results in an access violation exception.

The 
<b>VirtualFreeEx</b> function can release a range of pages that are in different states, some reserved and some committed. This means that you can release a range of pages without first determining the current commitment state of each page. The entire range of pages originally reserved by 
<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a> must be released at the same time.

If a page is released, its state changes to free, and it is available for subsequent allocation operations. After memory is released or decommitted, you can never refer to the memory again. Any information that may have been in that memory is gone forever. Attempts to read from or write to a free page results in an access violation exception. If you need to keep information, do not decommit or free memory that  contains the information.

The 
<b>VirtualFreeEx</b> function can be used on an AWE region of memory and it invalidates any physical page mappings in the region when freeing the address space. However, the physical pages are not deleted, and the application can use them. The application must explicitly call 
<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-freeuserphysicalpages">FreeUserPhysicalPages</a> to free the physical pages. When the  process is terminated, all resources are automatically cleaned up.

To delete an enclave when you finish using it, specify the following values:

<ul>
<li>The base address of the enclave for the <i>lpAddress</i> parameter.</li>
<li>0 for the <i>dwSize</i> parameter.</li>
<li><b>MEM_RELEASE</b> for the <i>dwFreeType</i> parameter. The <b>MEM_DECOMMIT</b> value is not supported for enclaves.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Memory/virtual-memory-functions">Virtual Memory Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a>
 

 

