---
UID: NF:memoryapi.MapViewOfFile3FromApp
title: MapViewOfFile3FromApp function
author: windows-sdk-content
description: Maps a view of a file mapping into the address space of a calling Windows Store app.
old-location: base\mapviewoffile3fromapp.htm
tech.root: memory
ms.assetid: 5E10E1B2-69D9-4F68-8F06-D411CF7FE2ED
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: MEM_LARGE_PAGES, MEM_REPLACE_PLACEHOLDER, MEM_RESERVE, MapViewOfFile3FromApp, MapViewOfFile3FromApp function, base.mapviewoffile3fromapp, memoryapi/MapViewOfFile3FromApp
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
 - MapViewOfFile3FromApp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MapViewOfFile3FromApp
: 
---

# MapViewOfFile3FromApp function


## -description


Maps a view of a file mapping into the address space of a calling 
    Windows Store app.

Using this function, you can: for new allocations, specify a range of virtual address space and a power-of-2 alignment restriction; specify an arbitrary number of extended parameters; specify a preferred NUMA node for the physical memory as an extended parameter; and specify a placeholder operation (specifically, replacement).

To specify the NUMA node, see the <i>ExtendedParameters</i> parameter.


## -parameters




### -param FileMapping [in]

A <b>HANDLE</b> to a section that is to be mapped
                        into the address space of the specified process.


### -param Process [in]

A <b>HANDLE</b> to a process into which the section
                    will be mapped.


### -param BaseAddress [in, optional]

The desired base address of the view.
                  The address is rounded down to the nearest 64k boundary.
                  If this parameter is <b>NULL</b>, the system picks the base
                  address.


### -param Offset [in]

The offset from the beginning of the section.
             This must be 64k aligned.


### -param ViewSize [in]

The number of bytes to map. A value of zero (0)
               specifies that the entire section is to be mapped.

The size must always be a multiple of the page size.


### -param AllocationType [in]

The type of memory allocation. This parameter can be zero (0) or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEM_RESERVE"></a><a id="mem_reserve"></a><dl>
<dt><b>MEM_RESERVE</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Maps a reserved view.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_REPLACE_PLACEHOLDER"></a><a id="mem_replace_placeholder"></a><dl>
<dt><b>MEM_REPLACE_PLACEHOLDER</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
 Replaces a placeholder with a mapped view. Only data/pf-backed section views are supported (no images, physical memory, etc.). When you replace a placeholder, <i>BaseAddress</i> and <i>ViewSize</i> must exactly match those of the placeholder.

After you replace a placeholder with a mapped view, to free that mapped view back to a placeholder, see the <i>UnmapFlags</i> parameter of <a href="https://msdn.microsoft.com/1C86075D-17B8-481E-BDF0-6E5A8F55C188">UnmapViewOfFileEx</a> and <a href="https://msdn.microsoft.com/300BA329-1E56-4C0F-81FC-FED42FCE9EB7">UnmapViewOfFile2</a>.

A placeholder is a type of reserved memory region.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_LARGE_PAGES"></a><a id="mem_large_pages"></a><dl>
<dt><b>MEM_LARGE_PAGES</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Maps a large page view. See <a href="https://msdn.microsoft.com/060115af-38d1-499c-b30c-47cd0cf42d20">large page support</a>.

</td>
</tr>
</table>
 


### -param PageProtection [in]

The desired page protection.

For file-mapping objects created with the <b>SEC_IMAGE</b> attribute, the 
       <i>PageProtection</i> parameter has no effect, and should be set to any valid value such as 
       <b>PAGE_READONLY</b>.


### -param ExtendedParameters [in, out, optional]

An optional pointer to one or more  extended parameters of type <a href="base.mem_extended_parameter">MEM_EXTENDED_PARAMETER</a>. Each of those extended parameter values can itself have a <i>Type</i> field of either <b>MemExtendedParameterAddressRequirements</b> or <b>MemExtendedParameterNumaNode</b>. If no <b>MemExtendedParameterNumaNode</b> extended parameter is provided, then the behavior is the same as for the <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>/<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a> functions (that is, the preferred NUMA node for the physical pages is determined based on the ideal processor of the thread that first accesses the memory).


### -param ParameterCount [in]

The number of extended parameters pointed to by <i>ExtendedParameters</i>.


## -returns



Returns the base address of the mapped view, if successful. Otherwise, returns <b>NULL</b> and extended error status is available
           using <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This API helps support high-performance games, and server applications, which have particular requirements around managing their virtual address space. For example, mapping memory on top of a previously reserved region; this is useful for implementing an automatically wrapping ring buffer. And allocating memory with specific alignment; for example, to enable your application to commit large/huge page-mapped regions on demand.


With one important exception, file views derived from any file mapping object that is backed by the same file 
    are coherent or identical at a specific time. Coherency is guaranteed for views within a process and for views 
    that are mapped by different processes.

The exception is related to remote files. Although 
    <b>MapViewOfFile3FromApp</b> works with remote files, it 
    does not keep them coherent. For example, if two computers both map a file as writable, and both change the same 
    page, each computer only sees its own writes to the page. When the data gets updated on the disk, it is not 
    merged.

 You can only successfully request executable protection if your app has the <b>codeGeneration</b> capability.


#### Examples

For a code example, see Scenario 1 in <a href="base.virtualalloc2">Virtual2Alloc</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d3302183-76a0-47ec-874f-1173db353dfe">CreateFileMapping</a>



<a href="https://msdn.microsoft.com/b1ebd9a4-cde4-4c0c-80d2-5ccb655cd3a4">Creating a File View</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a>



<a href="base.mapviewoffile3">MapViewOfFile3</a>



<a href="https://msdn.microsoft.com/2ac8a7d6-5c52-41de-acb9-d7f975fd2a94">MapViewOfFileEx</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/4896144c-78fc-4d21-a302-d9ba66fb2f8a">OpenFileMapping</a>



<a href="https://msdn.microsoft.com/971293b8-0af0-4bdf-a7d7-6b1bb80a469c">SYSTEM_INFO</a>



<a href="https://msdn.microsoft.com/2e9c3174-af48-4fa3-9f6a-fb62b23ed994">UnmapViewOfFile</a>
 

 

