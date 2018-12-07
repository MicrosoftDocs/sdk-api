---
UID: NF:memoryapi.VirtualAlloc2
title: VirtualAlloc2 function
author: windows-sdk-content
description: Reserves, commits, or changes the state of a region of memory within the virtual address space of a specified process. The function initializes the memory it allocates to zero.
old-location: base\virtualalloc2.htm
tech.root: memory
ms.assetid: 5021062F-E414-49A1-8B70-BE2A57A90E54
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MEM_COMMIT, MEM_LARGE_PAGES, MEM_PHYSICAL, MEM_REPLACE_PLACEHOLDER, MEM_RESERVE, MEM_RESERVE_PLACEHOLDER, MEM_RESET, MEM_RESET_UNDO, MEM_TOP_DOWN, VirtualAlloc2, VirtualAlloc2 function, base.virtualalloc2, memoryapi/VirtualAlloc2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - onecore.lib
api_name:
 - VirtualAlloc2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VirtualAlloc2 function


## -description


Reserves, commits, or changes the state  of a region of memory within the virtual address space of a specified process. The 
    function initializes the memory it allocates to zero.

Using this function, you can: for new allocations, specify a range of virtual address space and a power-of-2 alignment restriction; specify an arbitrary number of extended parameters; specify a preferred NUMA node for the physical memory as an extended parameter; and specify a placeholder operation (specifically, replacement).

To specify the NUMA node, see the <i>ExtendedParameters</i> parameter.


## -parameters




### -param Process [in, optional]

The handle to a process. The function allocates memory within the virtual address space of this process.

The handle must have the <b>PROCESS_VM_OPERATION</b> access right. For more information, 
       see 
       <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param BaseAddress [in, optional]

The pointer that specifies a desired starting address for the region of pages that you want to allocate.

 If an explicit base address is specified, then it must be a multiple of the system allocation granularity. To determine the size of a page and the allocation granularity on the host computer, use the 
       <a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a> function.

If <i>BaseAddress</i> is <b>NULL</b>, the function determines where to 
       allocate the region.

If this address is within an enclave that you have not initialized by calling <a href="https://msdn.microsoft.com/6A711135-A522-40AE-965F-E1AF97D0076A">InitializeEnclave</a>, <b>VirtualAlloc2</b> allocates a page of zeros for the enclave at that address. The page must be previously uncommitted, and will not be measured with the EEXTEND instruction of the Intel Software Guard Extensions programming model. 

If the address in within an enclave that you initialized, then the allocation operation fails with the <b>ERROR_INVALID_ADDRESS</b> error.


### -param Size [in]

The size of the region of memory to allocate, in bytes.

The size must always be a multiple of the page size.

If <i>BaseAddress</i> is not <b>NULL</b>, the function allocates all 
       pages that contain one or more bytes in the range from <i>BaseAddress</i> to 
       <i>BaseAddress</i>+<i>Size</i>. This means, for example, that a 2-byte 
       range that straddles a page boundary causes the function to allocate both pages.


### -param AllocationType [in]

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
         <b>VirtualAlloc2</b> with 
         <code>MEM_COMMIT | MEM_RESERVE</code>.

Attempting to commit a specific address range by specifying <b>MEM_COMMIT</b> without 
         <b>MEM_RESERVE</b> and a non-<b>NULL</b> <i>BaseAddress</i> fails unless the entire range has already been reserved. The resulting 
         error code is <b>ERROR_INVALID_ADDRESS</b>.

An attempt to commit a page that is already committed does not cause the function to fail. This means that 
         you can commit pages without first determining the current commitment state of each page.

If <i>BaseAddress</i> specifies an address within an enclave, <i>AllocationType</i> must be <b>MEM_COMMIT</b>.

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

You commit reserved pages by calling 
         <b>VirtualAlloc2</b> again with 
         <b>MEM_COMMIT</b>. To reserve and commit pages in one step, call 
         <b>VirtualAlloc2</b> with 
         <code>MEM_COMMIT | MEM_RESERVE</code>.

Other memory allocation functions, such as <b>malloc</b> and 
         <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>, cannot use reserved memory until it has 
        been released.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_REPLACE_PLACEHOLDER"></a><a id="mem_replace_placeholder"></a><dl>
<dt><b>MEM_REPLACE_PLACEHOLDER</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
 Replaces a placeholder with a normal private allocation. Only data/pf-backed section views are supported (no images, physical memory, etc.). When you replace a placeholder, <i>BaseAddress</i> and <i>Size</i> must exactly match those of the placeholder.

After you replace a placeholder with a private allocation, to free that allocation back to a placeholder, see the <i>dwFreeType</i> parameter of <a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a> and <a href="https://msdn.microsoft.com/2e5c862c-1251-49da-9c3a-90b09e488d89">VirtualFreeEx</a>.

A placeholder is a type of reserved memory region.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_RESERVE_PLACEHOLDER"></a><a id="mem_reserve_placeholder"></a><dl>
<dt><b>MEM_RESERVE_PLACEHOLDER</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
 To create a placeholder, call 
         <b>VirtualAlloc2</b> with 
         <code>MEM_RESERVE | MEM_RESERVE_PLACEHOLDER</code> and <i>PageProtection</i> set to <b>PAGE_NOACCESS</b>. To free/split/coalesce a placeholder, see the <i>dwFreeType</i> parameter of <a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a> and <a href="https://msdn.microsoft.com/2e5c862c-1251-49da-9c3a-90b09e488d89">VirtualFreeEx</a>.

A placeholder is a type of reserved memory region.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_RESET"></a><a id="mem_reset"></a><dl>
<dt><b>MEM_RESET</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Indicates that data in the memory range specified by <i>BaseAddress</i> and 
         <i>Size</i> is no longer of interest. The pages should not be read from or written to 
         the paging file. However, the memory block will be used again later, so it should not be decommitted. This 
         value cannot be used with any other value.

Using this value does not guarantee that the range operated on with <b>MEM_RESET</b> 
         will contain zeros. If you want the range to contain zeros, decommit the memory and then recommit it.

When you use <b>MEM_RESET</b>, the 
         <b>VirtualAlloc2</b> function ignores the value of 
         <i>fProtect</i>. However, you must still set <i>fProtect</i> to a valid 
         protection value, such as <b>PAGE_NOACCESS</b>.

<b>VirtualAlloc2</b> returns an error if you use 
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
         specified memory range specified by <i>BaseAddress</i> and <i>Size</i> 
         is of interest to the caller and attempts to reverse the effects of <b>MEM_RESET</b>. If 
         the function succeeds, that means all data in the specified address range is intact. If the function fails, 
         at least some of the data in the address range has been replaced with zeroes.

This value cannot be used with any other value. If <b>MEM_RESET_UNDO</b> is called on an 
         address range which was not <b>MEM_RESET</b> earlier, the behavior is undefined. When you 
         specify <b>MEM_RESET</b>, the 
         <b>VirtualAlloc2</b> function ignores the value of 
         <i>PageProtection</i>. However, you must still set <i>PageProtection</i> to a 
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
</table>
 


### -param PageProtection [in]

The memory protection for the region of pages to be allocated. If the pages are being committed, you can 
      specify any one of the 
      <a href="https://msdn.microsoft.com/09839db7-2118-4a7d-a707-a08c92bd600c">memory protection constants</a>.

If <i>BaseAddress</i> specifies an address within an enclave, <i>PageProtection</i> cannot be any of the following values:

<ul>
<li>PAGE_NOACCESS</li>
<li>PAGE_GUARD</li>
<li>PAGE_NOCACHE</li>
<li>PAGE_WRITECOMBINE</li>
</ul>

### -param ExtendedParameters [in, out, optional]

An optional pointer to one or more  extended parameters of type <a href="base.mem_extended_parameter">MEM_EXTENDED_PARAMETER</a>. Each of those extended parameter values can itself have a <i>Type</i> field of either <b>MemExtendedParameterAddressRequirements</b> or <b>MemExtendedParameterNumaNode</b>. If no <b>MemExtendedParameterNumaNode</b> extended parameter is provided, then the behavior is the same as for the <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>/<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a> functions (that is, the preferred NUMA node for the physical pages is determined based on the ideal processor of the thread that first accesses the memory).


### -param ParameterCount [in]

The number of extended parameters pointed to by <i>ExtendedParameters</i>.


## -returns



If the function succeeds, the return value is the base address of the allocated region of pages.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This API helps support high-performance games, and server applications, which have particular requirements around managing their virtual address space. For example, mapping memory on top of a previously reserved region; this is useful for implementing an automatically wrapping ring buffer. And allocating memory with specific alignment; for example, to enable your application to commit large/huge page-mapped regions on demand.


Each page has an associated <a href="https://msdn.microsoft.com/a6faa901-2966-4556-90ef-c113b1ba6c6d">page state</a>. The 
     <b>VirtualAlloc2</b> function can perform the following 
     operations:

<ul>
<li>Commit a region of reserved pages</li>
<li>Reserve a region of free pages</li>
<li>Simultaneously reserve and commit a region of free pages</li>
</ul>
<b>VirtualAlloc2</b> cannot reserve a reserved page. It 
    can commit a page that is already committed. This means you can commit a range of pages, regardless of whether 
    they have already been committed, and the function will not fail.

You can use <b>VirtualAlloc2</b> to reserve a block of 
    pages and then make additional calls to <b>VirtualAlloc2</b> 
    to commit individual pages from the reserved block. This enables a process to reserve a range of its virtual 
    address space without consuming physical storage until it is needed.

If the <i>lpAddress</i> parameter is not <b>NULL</b>, the function uses 
    the <i>lpAddress</i> and <i>dwSize</i> parameters to compute the region of 
    pages to be allocated. The current state of the entire range of pages must be compatible with the type of 
    allocation specified by the <i>flAllocationType</i> parameter. Otherwise, the function fails 
    and none of the pages is allocated. This compatibility requirement does not preclude committing an already 
    committed page; see the preceding list.

To execute dynamically generated code, use 
    <b>VirtualAlloc2</b> to allocate memory, and the 
    <a href="https://msdn.microsoft.com/6afd7ae6-e4c5-483c-a638-c85781674c7b">VirtualProtectEx</a> function to grant 
    <b>PAGE_EXECUTE</b> access.

The <b>VirtualAlloc2</b> function can be used to reserve 
    an <a href="https://msdn.microsoft.com/48a29922-8130-4540-86b0-0faa120566a6">Address Windowing Extensions</a> 
    (AWE) region of memory within the virtual address space of a specified process. This region of memory can then be 
    used to map physical pages into and out of virtual memory as required by the application. The 
    <b>MEM_PHYSICAL</b> and <b>MEM_RESERVE</b> values must be set in the 
    <i>AllocationType</i> parameter. The <b>MEM_COMMIT</b> value must not be 
    set. The page protection must be set to <b>PAGE_READWRITE</b>.

The <a href="https://msdn.microsoft.com/2e5c862c-1251-49da-9c3a-90b09e488d89">VirtualFreeEx</a> function can decommit a committed 
    page, releasing the page's storage, or it can simultaneously decommit and release a committed page. It can also 
    release a reserved page, making it a free page.

When creating a region that will be executable, the calling program bears responsibility for ensuring cache 
    coherency via an appropriate call to 
    <a href="https://msdn.microsoft.com/6267adde-8169-4673-97ec-78c66e2135c1">FlushInstructionCache</a> once the code has been set 
    in place. Otherwise attempts to execute code out of the newly executable region may produce unpredictable 
    results.


#### Examples

Scenario 1. Create a circular buffer by mapping two adjacent views of the same shared memory section.


```cpp
#include <windows.h>
#include <stdio.h>
#include <stdlib.h>

//
// This function creates a ring buffer by allocating a pagefile-backed section
// and mapping two views of that section next to each other. This way if the
// last record in the buffer wraps it can still be accessed in a linear fashion
// using its base VA.
//

void*
CreateRingBuffer (
    unsigned int bufferSize,
    _Outptr_ void** secondaryView
    )
{
    BOOL result;
    HANDLE section = nullptr;
    SYSTEM_INFO sysInfo;
    void* ringBuffer = nullptr;
    void* placeholder1 = nullptr;
    void* placeholder2 = nullptr;
    void* view1 = nullptr;
    void* view2 = nullptr;

    GetSystemInfo (&sysInfo);

    if ((bufferSize % sysInfo.dwAllocationGranularity) != 0) {
        return nullptr;
    }

    //
    // Reserve a placeholder region where the buffer will be mapped.
    //

    placeholder1 = (PCHAR) VirtualAlloc2 (
        nullptr,
        nullptr,
        2 * bufferSize,
        MEM_RESERVE | MEM_RESERVE_PLACEHOLDER,
        PAGE_NOACCESS,
        nullptr, 0
    );

    if (placeholder1 == nullptr) {
        printf ("VirtualAlloc2 failed, error %#x\n", GetLastError());
        goto Exit;
    }

    //
    // Split the placeholder region into two regions of equal size.
    //

    result = VirtualFree (
        placeholder1,
        bufferSize,
        MEM_RELEASE | MEM_PRESERVE_PLACEHOLDER
    );

    if (result == FALSE) {
        printf ("VirtualFreeEx failed, error %#x\n", GetLastError());
        goto Exit;
    }

    placeholder2 = (void*) ((ULONG_PTR) placeholder1 + bufferSize);

    //
    // Create a pagefile-backed section for the buffer.
    //

    section = CreateFileMapping (
        INVALID_HANDLE_VALUE,
        nullptr,
        PAGE_READWRITE,
        0,
        bufferSize, nullptr
    );

    if (section == nullptr) {
        printf ("CreateFileMapping failed, error %#x\n", GetLastError());
        goto Exit;
    }

    //
    // Map the section into the first placeholder region.
    //

    view1 = MapViewOfFile3 (
        section,
        nullptr,
        placeholder1,
        0,
        bufferSize,
        MEM_REPLACE_PLACEHOLDER,
        PAGE_READWRITE,
        nullptr, 0
    );

    if (view1 == nullptr) {
        printf ("MapViewOfFile3 failed, error %#x\n", GetLastError());
        goto Exit;
    }

    //
    // Ownership transferred, don’t free this now.
    //

    placeholder1 = nullptr;

    //
    // Map the section into the second placeholder region.
    //

    view2 = MapViewOfFile3 (
        section,
        nullptr,
        placeholder2,
        0,
        bufferSize,
        MEM_REPLACE_PLACEHOLDER,
        PAGE_READWRITE,
        nullptr, 0
    );

    if (view2 == nullptr) {
        printf ("MapViewOfFile3 failed, error %#x\n", GetLastError());
        goto Exit;
    }

    //
    // Success, return both mapped views to the caller.
    //

    ringBuffer = view1;
    *secondaryView = view2;

    placeholder2 = nullptr;
    view1 = nullptr;
    view2 = nullptr;

Exit:

    if (section != nullptr) {
        CloseHandle (section);
    }

    if (placeholder1 != nullptr) {
        VirtualFree (placeholder1, 0, MEM_RELEASE);
    }

    if (placeholder2 != nullptr) {
        VirtualFree (placeholder2, 0, MEM_RELEASE);
    }

    if (view1 != nullptr) {
        UnmapViewOfFileEx (view1, 0);
    }

    if (view2 != nullptr) {
        UnmapViewOfFileEx (view2, 0);
    }

    return ringBuffer;
}

int __cdecl wmain()
{
    char* ringBuffer;
    void* secondaryView;
    unsigned int bufferSize = 0x10000;

    ringBuffer = (char*) CreateRingBuffer (bufferSize, &secondaryView);

    if (ringBuffer == nullptr) {
        printf ("CreateRingBuffer failed\n");
        return 0;
    }

    //
    // Make sure the buffer wraps properly.
    //

    ringBuffer[0] = 'a';

    if (ringBuffer[bufferSize] == 'a') {
        printf ("The buffer wraps as expected\n");
    }

    UnmapViewOfFile (ringBuffer);
    UnmapViewOfFile (secondaryView);
}

```


Scenario 2. Specify a preferred NUMA node when allocating memory.


```cpp

void*
AllocateWithPreferredNode (size_t size, unsigned int numaNode)
{
    MEM_EXTENDED_PARAMETER param = {0};

    param.Type = MemExtendedParameterNumaNode;
    param.ULong = numaNode;

    return VirtualAlloc2 (
        nullptr, nullptr,
        size,
        MEM_RESERVE | MEM_COMMIT,
        PAGE_READWRITE,
        &param, 1);
}

```


Scenario 3. Allocate memory in a specific virtual address range (below 4GB, in this example) and with specific alignment.


```cpp

void*
AllocateAlignedBelow2GB (size_t size, size_t alignment)
{
    MEM_ADDRESS_REQUIREMENTS addressReqs = {0};
    MEM_EXTENDED_PARAMETER param = {0};

    addressReqs.Alignment = alignment;
    addressReqs.HighestEndingAddress = (PVOID)(ULONG_PTR) 0x7fffffff;

    param.Type = MemExtendedParameterAddressRequirements;
    param.Pointer = &addressReqs;

    return VirtualAlloc2 (
        nullptr, nullptr,
        size,
        MEM_RESERVE | MEM_COMMIT,
        PAGE_READWRITE,
        &param, 1);
}

```





## -see-also




<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/8774e145-ee7f-44de-85db-0445b905f986">ReadProcessMemory</a>



<a href="https://msdn.microsoft.com/9488a854-1ef0-488f-b3d1-57c1acb82a88">Virtual Memory Functions</a>



<a href="https://msdn.microsoft.com/dcafd557-834e-4fdf-9cb2-aad76109ad92">VirtualAllocExNuma</a>



<a href="https://msdn.microsoft.com/2e5c862c-1251-49da-9c3a-90b09e488d89">VirtualFreeEx</a>



<a href="https://msdn.microsoft.com/414c4704-36f2-40f9-a69a-9d53ab354c30">VirtualLock</a>



<a href="https://msdn.microsoft.com/a0018bba-226b-4c18-8ea4-15e69524db11">VirtualProtect</a>



<a href="https://msdn.microsoft.com/3b1f7d27-1f5d-452e-b58f-560cd9b9cbd3">VirtualQuery</a>



<a href="https://msdn.microsoft.com/9cd91f1c-58ce-4adc-b027-45748543eb06">WriteProcessMemory</a>
 

 

