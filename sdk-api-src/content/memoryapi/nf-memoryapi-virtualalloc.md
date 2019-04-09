---
UID: NF:memoryapi.VirtualAlloc
title: VirtualAlloc function (memoryapi.h)
author: windows-sdk-content
description: Reserves, commits, or changes the state of a region of pages in the virtual address space of the calling process.
old-location: base\virtualalloc.htm
tech.root: Memory
ms.assetid: a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MEM_COMMIT, MEM_LARGE_PAGES, MEM_PHYSICAL, MEM_RESERVE, MEM_RESET, MEM_RESET_UNDO, MEM_TOP_DOWN, MEM_WRITE_WATCH, VirtualAlloc, VirtualAlloc function, _win32_virtualalloc, base.virtualalloc, winbase/VirtualAlloc
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
 - API-MS-Win-Core-memory-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - VirtualAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VirtualAlloc function


## -description


Reserves, commits, or changes the state  of a region of pages in the virtual address space of the calling process. 
    Memory allocated by this function is automatically initialized to zero.

To allocate memory in the address space of another process, use the 
    <a href="https://msdn.microsoft.com/ff0b6b79-40f5-499c-b797-b66797654164">VirtualAllocEx</a> function.


## -parameters




### -param lpAddress [in, optional]

The starting address of the region to allocate. If the memory is being reserved, the specified address is 
      rounded down to the nearest multiple of the allocation granularity. If the memory is already reserved and is 
      being committed, the address is rounded down to the next page boundary. To determine the size of a page and the 
      allocation granularity on the host computer, use the 
      <a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a> function. If this parameter is 
      <b>NULL</b>, the system determines where to allocate the region.

If this address is within an enclave that you have not initialized by calling <a href="https://msdn.microsoft.com/6A711135-A522-40AE-965F-E1AF97D0076A">InitializeEnclave</a>, <b>VirtualAlloc</b> allocates a page of zeros for the enclave at that address. The page must be previously uncommitted, and will not be measured with the EEXTEND instruction of the Intel Software Guard Extensions programming model. 

If the address in within an enclave that you initialized, then the allocation operation fails with the <b>ERROR_INVALID_ADDRESS</b> error.


### -param dwSize [in]

The size of the region, in bytes. If the <i>lpAddress</i> parameter is 
      <b>NULL</b>, this value is rounded up to the next page boundary. Otherwise, the allocated 
      pages include all pages containing one or more bytes in the range from <i>lpAddress</i> to 
      <i>lpAddress</i>+<i>dwSize</i>. This means that a 2-byte range straddling 
      a page boundary causes both pages to be included in the allocated region.


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

To reserve and commit pages in one step, call 
         <b>VirtualAlloc</b> with 
         <code>MEM_COMMIT | MEM_RESERVE</code>.

Attempting to commit a specific address range by specifying <b>MEM_COMMIT</b> without 
         <b>MEM_RESERVE</b> and a non-<b>NULL</b> <i>lpAddress</i> fails unless the entire range has already been reserved. The  resulting 
         error code is <b>ERROR_INVALID_ADDRESS</b>.

An attempt to commit a page that is 
         already committed does not cause the function to fail. This means that you can commit pages without first 
         determining the current commitment state of each page.

If <i>lpAddress</i> specifies an address within an enclave, <i>flAllocationType</i> must be <b>MEM_COMMIT</b>.

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

You can commit reserved pages in subsequent calls to the 
         <b>VirtualAlloc</b> function. To reserve and commit pages 
         in one step, call <b>VirtualAlloc</b> with 
         <b>MEM_COMMIT</b> | <b>MEM_RESERVE</b>.

Other memory allocation functions, such as <b>malloc</b> and 
         <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>, cannot use a reserved range of memory 
         until it is released.

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

When you specify <b>MEM_RESET</b>, the 
         <b>VirtualAlloc</b> function ignores the value of 
         <i>flProtect</i>. However, you must still set <i>flProtect</i> to a 
         valid protection value, such as <b>PAGE_NOACCESS</b>.

<b>VirtualAlloc</b> returns an error if you use 
         <b>MEM_RESET</b> and the range of memory is mapped to a file. A shared view is only 
         acceptable if it is mapped to a paging file.

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
         <b>VirtualAlloc</b> function ignores the value of 
         <i>flProtect</i>. However, you must still set <i>flProtect</i> to a 
         valid protection value, such as <b>PAGE_NOACCESS</b>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>The <b>MEM_RESET_UNDO</b> flag is not supported until Windows 8 and 
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
Allocates memory using <a href="https://msdn.microsoft.com/060115af-38d1-499c-b30c-47cd0cf42d20">large page support</a>.

The size and alignment must be a multiple of the large-page minimum. To obtain this value, use the 
         <a href="https://msdn.microsoft.com/ccde687d-ee8f-4668-93c1-a1fece86c2f6">GetLargePageMinimum</a> function.

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
         <a href="https://msdn.microsoft.com/48a29922-8130-4540-86b0-0faa120566a6">Address Windowing Extensions</a> (AWE) 
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
Allocates memory at the highest possible address. This can be slower than regular allocations, especially 
        when there are many allocations.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_WRITE_WATCH"></a><a id="mem_write_watch"></a><dl>
<dt><b>MEM_WRITE_WATCH</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
Causes the system to track pages that are written to in the allocated region. If you specify this value, 
         you must also specify <b>MEM_RESERVE</b>.

To retrieve the addresses of the pages that have been written to since the region was allocated or the 
         write-tracking state was reset, call the 
         <a href="https://msdn.microsoft.com/fa1426fe-4a1d-4300-b6f3-3e9e2272b8d3">GetWriteWatch</a> function. To reset the write-tracking 
         state, call <b>GetWriteWatch</b> or 
         <a href="https://msdn.microsoft.com/afbc5a58-01e2-4f32-bc47-351fe846e4a5">ResetWriteWatch</a>. The write-tracking feature 
         remains enabled for the memory region until the region is freed.

</td>
</tr>
</table>
 


### -param flProtect [in]

The memory protection for the region of pages to be allocated. If the pages are being committed, you can 
      specify any one of the 
      <a href="https://msdn.microsoft.com/09839db7-2118-4a7d-a707-a08c92bd600c">memory protection constants</a>.

If <i>lpAddress</i> specifies an address within an enclave, <i>flProtect</i> cannot be any of the following values:

<ul>
<li>PAGE_NOACCESS</li>
<li>PAGE_GUARD</li>
<li>PAGE_NOCACHE</li>
<li>PAGE_WRITECOMBINE</li>
</ul>

## -returns



If the function succeeds, the return value is the base address of the allocated region of pages.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Each page has an associated <a href="https://msdn.microsoft.com/a6faa901-2966-4556-90ef-c113b1ba6c6d">page state</a>. The 
    <b>VirtualAlloc</b> function can perform the following 
    operations:

<ul>
<li>Commit a region of reserved pages</li>
<li>Reserve a region of free pages</li>
<li>Simultaneously reserve and commit a region of free pages</li>
</ul>
<b>VirtualAlloc</b> cannot reserve a reserved page. It can 
    commit a page that is already committed. This means you can commit a range of pages, regardless of whether they 
    have already been committed, and the function will not fail.

You can use <b>VirtualAlloc</b> to reserve a block of pages 
    and then make additional calls to <b>VirtualAlloc</b> to commit 
    individual pages from the reserved block. This enables a process to reserve a range of its virtual address space 
    without consuming physical storage until it is needed.

If the <i>lpAddress</i> parameter is not <b>NULL</b>, the function uses 
    the <i>lpAddress</i> and <i>dwSize</i> parameters to compute the region of 
    pages to be allocated. The current state of the entire range of pages must be compatible with the type of 
    allocation specified by the <i>flAllocationType</i> parameter. Otherwise, the function fails 
    and none of the pages are allocated. This compatibility requirement does not preclude committing an already 
    committed page, as mentioned previously.

To execute dynamically generated code, use 
    <b>VirtualAlloc</b> to allocate memory and the 
    <a href="https://msdn.microsoft.com/a0018bba-226b-4c18-8ea4-15e69524db11">VirtualProtect</a> function to grant 
    <b>PAGE_EXECUTE</b> access.

The <b>VirtualAlloc</b> function can be used to reserve an 
    <a href="https://msdn.microsoft.com/48a29922-8130-4540-86b0-0faa120566a6">Address Windowing Extensions</a> (AWE) 
    region of memory within the virtual address space of a specified process. This region of memory can then be used 
    to map physical pages into and out of virtual memory as required by the application. The 
    <b>MEM_PHYSICAL</b> and <b>MEM_RESERVE</b> values must be set in the 
    <i>AllocationType</i> parameter. The <b>MEM_COMMIT</b> value must not be 
    set. The page protection must be set to <b>PAGE_READWRITE</b>.

The <a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a> function can decommit a committed 
    page, releasing the page's storage, or it can simultaneously decommit and release a committed page. It can also 
    release a reserved page, making it a free page.

When creating a region that will be executable, the calling program bears responsibility for ensuring cache 
    coherency via an appropriate call to 
    <a href="https://msdn.microsoft.com/6267adde-8169-4673-97ec-78c66e2135c1">FlushInstructionCache</a> once the code has been set 
    in place. Otherwise attempts to execute code out of the newly executable region may produce unpredictable 
    results.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/f46bd57d-7684-4a08-8ac7-de204aecb207">Reserving and Committing Memory</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/9488a854-1ef0-488f-b3d1-57c1acb82a88">Virtual Memory Functions</a>



<a href="https://msdn.microsoft.com/ff0b6b79-40f5-499c-b797-b66797654164">VirtualAllocEx</a>



<a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a>



<a href="https://msdn.microsoft.com/414c4704-36f2-40f9-a69a-9d53ab354c30">VirtualLock</a>



<a href="https://msdn.microsoft.com/a0018bba-226b-4c18-8ea4-15e69524db11">VirtualProtect</a>



<a href="https://msdn.microsoft.com/3b1f7d27-1f5d-452e-b58f-560cd9b9cbd3">VirtualQuery</a>
 

 

