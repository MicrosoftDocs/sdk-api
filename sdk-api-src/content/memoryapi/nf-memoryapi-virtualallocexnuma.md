---
UID: NF:memoryapi.VirtualAllocExNuma
title: VirtualAllocExNuma function (memoryapi.h)
description: Reserves, commits, or changes the state of a region of memory within the virtual address space of the specified process, and specifies the NUMA node for the physical memory.
helpviewer_keywords: ["MEM_COMMIT","MEM_LARGE_PAGES","MEM_PHYSICAL","MEM_RESERVE","MEM_RESET","MEM_RESET_UNDO","MEM_TOP_DOWN","VirtualAllocExNuma","VirtualAllocExNuma function","base.virtualallocexnuma","winbase/VirtualAllocExNuma"]
old-location: base\virtualallocexnuma.htm
tech.root: base
ms.assetid: dcafd557-834e-4fdf-9cb2-aad76109ad92
ms.date: 12/05/2018
ms.keywords: MEM_COMMIT, MEM_LARGE_PAGES, MEM_PHYSICAL, MEM_RESERVE, MEM_RESET, MEM_RESET_UNDO, MEM_TOP_DOWN, VirtualAllocExNuma, VirtualAllocExNuma function, base.virtualallocexnuma, winbase/VirtualAllocExNuma
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
 - VirtualAllocExNuma
 - memoryapi/VirtualAllocExNuma
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
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - VirtualAllocExNuma
---

# VirtualAllocExNuma function


## -description

Reserves, commits, or changes the state  of a region of memory within the virtual address space of the specified process, and 
    specifies the NUMA node for the physical memory.

## -parameters

### -param hProcess [in]

The handle to a process. The function allocates memory within the virtual address space of this process.

The handle must have the <b>PROCESS_VM_OPERATION</b> access right. For more information, 
       see 
       <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param lpAddress [in, optional]

The pointer that specifies a desired starting address for the region of pages that you want to allocate.

If you are reserving memory, the function rounds this address down to the nearest multiple of the allocation 
       granularity.

If you are committing memory that is already reserved, the function rounds this address down to the nearest 
       page boundary. To determine the size of a page and the allocation granularity on the host computer, use the 
       <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function.

If <i>lpAddress</i> is <b>NULL</b>, the function determines where to 
       allocate the region.

### -param dwSize [in]

The size of the region of memory to be allocated, in bytes.

If <i>lpAddress</i> is <b>NULL</b>, the function rounds 
       <i>dwSize</i> up to the next page boundary.

If <i>lpAddress</i> is not <b>NULL</b>, the function allocates all 
       pages that contain one or more bytes in the range from <i>lpAddress</i> to 
       <code>(lpAddress+dwSize)</code>. This means, for example, that a 2-byte 
       range that straddles a page boundary causes the function to allocate both pages.

### -param flAllocationType [in]

The type of memory allocation. This parameter must contain one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEM_COMMIT"></a><a id="mem_commit"></a><dl>
<dt><b>MEM_COMMIT</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Allocates memory charges (from the overall size of memory and the paging files on disk) for the specified 
         reserved memory pages. The function also guarantees that when the caller later initially accesses the memory, 
         the contents will be zero.  Actual physical pages are not allocated unless/until the virtual addresses are 
         actually accessed.

To reserve and commit pages in one step, call the function with 
         <code>MEM_COMMIT | MEM_RESERVE</code>.

Attempting to commit a specific address range by specifying <b>MEM_COMMIT</b> without 
         <b>MEM_RESERVE</b> and a non-<b>NULL</b> <i>lpAddress</i> fails unless the entire range has already been reserved. The resulting 
         error code is <b>ERROR_INVALID_ADDRESS</b>.

An attempt to commit a page that is already committed does not cause the function to fail. This means that 
         you can commit pages without first determining the current commitment state of each page.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_RESERVE"></a><a id="mem_reserve"></a><dl>
<dt><b>MEM_RESERVE</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Reserves a range of the process's virtual address space without allocating any actual physical storage in 
         memory or in the paging file on disk.

You commit reserved pages by calling the function again with <b>MEM_COMMIT</b>. To 
         reserve and commit pages in one step, call the function with 
         <code>MEM_COMMIT | MEM_RESERVE</code>.

Other memory allocation functions, such as <b>malloc</b> and 
         <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>, cannot use reserved memory until it has 
         been released.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_RESET"></a><a id="mem_reset"></a><dl>
<dt><b>MEM_RESET</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Indicates that data in the memory range specified by <i>lpAddress</i> and 
         <i>dwSize</i> is no longer of interest. The pages should not be read from or written to 
         the paging file. However, the memory block will be used again later, so it should not be decommitted. This 
         value cannot be used with any other value.

Using this value does not guarantee that the range operated on with <b>MEM_RESET</b> 
         will contain zeros. If you want the range to contain zeros, decommit the memory and then recommit it.

When you use <b>MEM_RESET</b>, the function ignores the value of 
         <i>fProtect</i>. However, you must still set <i>fProtect</i> to a valid 
         protection value, such as <b>PAGE_NOACCESS</b>.

The function returns an error if you use <b>MEM_RESET</b> and the range of memory is 
         mapped to a file. A shared view is only acceptable if it is mapped to a paging file.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_RESET_UNDO"></a><a id="mem_reset_undo"></a><dl>
<dt><b>MEM_RESET_UNDO</b></dt>
<dt>0x1000000</dt>
</dl>
</td>
<td width="60%">
<b>MEM_RESET_UNDO</b> should only be called on an address range to which 
         <b>MEM_RESET</b> was successfully applied earlier. It indicates that the data in the 
         specified memory range specified by <i>lpAddress</i> and <i>dwSize</i> 
         is of interest to the caller and attempts to reverse the effects of <b>MEM_RESET</b>. If 
         the function succeeds, that means all data in the specified address range is intact. If the function fails, 
         at least some of the data in the address range has been replaced with zeroes.

This value cannot be used with any other value. If <b>MEM_RESET_UNDO</b> is called on an 
         address range which was not <b>MEM_RESET</b> earlier, the behavior is undefined. When you 
         specify <b>MEM_RESET</b>, the 
         <b>VirtualAllocExNuma</b> function ignores the value of 
         <i>flProtect</i>. However, you must still set <i>flProtect</i> to a 
         valid protection value, such as <b>PAGE_NOACCESS</b>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>The <b>MEM_RESET_UNDO</b> flag is not supported until Windows 8 and 
          Windows Server 2012.

</td>
</tr>
</table>
 

This parameter can also specify the following values as indicated.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEM_LARGE_PAGES"></a><a id="mem_large_pages"></a><dl>
<dt><b>MEM_LARGE_PAGES</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Allocates memory using <a href="/windows/desktop/Memory/large-page-support">large page support</a>.

The size and alignment must be a multiple of the large-page minimum. To obtain this value, use the 
         <a href="/windows/desktop/api/memoryapi/nf-memoryapi-getlargepageminimum">GetLargePageMinimum</a> function.

If you specify this value, you must also specify <b>MEM_RESERVE</b> and <b>MEM_COMMIT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_PHYSICAL"></a><a id="mem_physical"></a><dl>
<dt><b>MEM_PHYSICAL</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
Reserves an address range that can be used to map 
         <a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a> (AWE) 
         pages.

This value must be used with <b>MEM_RESERVE</b> and no other values.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_TOP_DOWN"></a><a id="mem_top_down"></a><dl>
<dt><b>MEM_TOP_DOWN</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Allocates memory at the highest possible address.

</td>
</tr>
</table>

### -param flProtect [in]

The memory protection for the region of pages to be allocated. If the pages are being committed, you can 
       specify any one of the 
       <a href="/windows/desktop/Memory/memory-protection-constants">memory protection constants</a>.

Protection attributes specified when protecting a page cannot conflict with those specified when allocating 
       a page.

### -param nndPreferred [in]

The NUMA node where the physical memory should reside.

Used only when allocating a new VA region (either committed or reserved). Otherwise this parameter is ignored 
       when the API is used to commit pages in a region that already exists

## -returns

If the function succeeds, the return value is the base address of the allocated region of pages.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Each page has an associated <a href="/windows/desktop/Memory/page-state">page state</a>. The 
     <b>VirtualAllocExNuma</b> function can perform the 
     following operations:


<ul>
<li>Commit a region of reserved pages</li>
<li>Reserve a region of free pages</li>
<li>Simultaneously reserve and commit a region of free pages</li>
</ul>


<b>VirtualAllocExNuma</b> cannot reserve a reserved 
     page. It can commit a page that is already committed. This means you can commit a range of pages, regardless of 
     whether they have already been committed, and the function will not fail.

You can use <b>VirtualAllocExNuma</b> to reserve a 
     block of pages and then make additional calls to 
     <b>VirtualAllocExNuma</b> to commit individual pages from 
     the reserved block. This enables a process to reserve a range of its virtual address space without consuming 
     physical storage until it is needed.

If the <i>lpAddress</i> parameter is not <b>NULL</b>, the function uses 
     the <i>lpAddress</i> and <i>dwSize</i> parameters to compute the region of 
     pages to be allocated. The current state of the entire range of pages must be compatible with the type of 
     allocation specified by the <i>flAllocationType</i> parameter. Otherwise, the function fails 
     and none of the pages is allocated. This compatibility requirement does not preclude committing an already 
     committed page; see the preceding list.

Because <b>VirtualAllocExNuma</b> does not allocate any 
     physical pages, it will succeed whether or not the pages are available on that node or elsewhere in the system. 
     The physical pages are allocated on demand. If the preferred node runs out of pages, the memory manager will use 
     pages from other nodes. If the memory is paged out, the same process is used when it is brought back in.

To execute dynamically generated code, use 
     <b>VirtualAllocExNuma</b> to allocate memory and the 
     <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotectex">VirtualProtectEx</a> function to grant 
     <b>PAGE_EXECUTE</b> access.

The <b>VirtualAllocExNuma</b> function can be used to 
     reserve an 
     <a href="/windows/desktop/Memory/address-windowing-extensions">Address Windowing Extensions</a> 
     (AWE) region of memory within the virtual address space of a specified process. This region of memory can then be 
     used to map physical pages into and out of virtual memory as required by the application. The 
     <b>MEM_PHYSICAL</b> and <b>MEM_RESERVE</b> values must be set in the 
     <i>AllocationType</i> parameter. The <b>MEM_COMMIT</b> value must not be 
     set. The page protection must be set to <b>PAGE_READWRITE</b>.

The <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfreeex">VirtualFreeEx</a> function can decommit a committed 
     page, releasing the page's storage, or it can simultaneously decommit and release a committed page. It can also 
     release a reserved page, making it a free page.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 
     or later.


#### Examples

For an example, see 
     <a href="/windows/desktop/Memory/allocating-memory-from-a-numa-node">Allocating Memory from a NUMA Node</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>



<a href="/windows/desktop/Memory/virtual-memory-functions">Virtual Memory Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfreeex">VirtualFreeEx</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtuallock">VirtualLock</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect">VirtualProtect</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualquery">VirtualQuery</a>