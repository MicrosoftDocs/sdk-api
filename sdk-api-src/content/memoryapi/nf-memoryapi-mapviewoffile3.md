---
UID: NF:memoryapi.MapViewOfFile3
title: MapViewOfFile3 function
author: windows-sdk-content
description: Maps a view of a file or a pagefile-backed section into the address space of the specified process.
old-location: base\mapviewoffile3.htm
tech.root: Memory
ms.assetid: 585D7BA1-688F-4F24-8D8D-46A2FC137193
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MapViewOfFile3, MapViewOfFile3 function, base.mapviewoffile3, memoryapi/MapViewOfFile3
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
 - MapViewOfFile3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MapViewOfFile3 function


## -description


Maps a view of a file or a pagefile-backed section into the address
    space of the specified process.

Using this function you can: allocate/map memory with specified power-of-2 alignment; allocate/map memory in a specified range of virtual address space; and allocate/map memory on top of a previously reserved range.

To specify the NUMA node for the physical memory, see the <i>ExtendedParameters</i> parameter.


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


### -param AllocationType [in]

The type of allocation. This parameter can be zero (0) or one of the following constant values:

<ul>
<li><b>MEM_RESERVE</b> - Maps a reserved view</li>
<li><b>MEM_LARGE_PAGES</b> - Maps a large page view</li>
</ul>

### -param PageProtection [in]

The desired page protection.


### -param ExtendedParameters [in, out, optional]

An optional pointer to one or more  extended parameters of type <a href="base.mem_extended_parameter">MEM_EXTENDED_PARAMETER</a>. Each of those extended parameter values can itself have a <i>Type</i> field of either <b>MemExtendedParameterAddressRequirements</b> or <b>MemExtendedParameterNumaNode</b>. If no <b>MemExtendedParameterNumaNode</b> extended parameter is provided, then the behavior is the same as for the <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>/<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a> functions (that is, the preferred NUMA node for the physical pages is determined based on the ideal processor of the thread that first accesses the memory).


### -param ParameterCount [in]

The number of extended parameters pointed to by <i>ExtendedParameters</i>.


## -returns



Returns the base address of the mapped view, if successful. Otherwise, returns <b>NULL</b> and extended error status is available
           using <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This API helps support high-performance games, and server applications, which have particular requirements around managing their virtual address space. For example, mapping memory on top of a previously reserved region; this is useful for implementing an automatically wrapping ring buffer. And allocating memory with specific alignment; for example, to enable your application to commit large/huge page-mapped regions on demand.



#### Examples

For a code example, see Scenario 1 in <a href="base.virtualalloc2">Virtual2Alloc</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>



<a href="https://msdn.microsoft.com/D97138F0-2FB3-488A-91AC-A654B22FE9AD">MapViewOfFile2</a>



<a href="https://msdn.microsoft.com/848BF3AD-9469-4A16-B1C4-B5D78954D9B5">MapViewOfFileNuma2</a>
 

 

