---
UID: NF:memoryapi.MapViewOfFile3
title: MapViewOfFile3 function (memoryapi.h)
description: Maps a view of a file or a pagefile-backed section into the address space of the specified process. (MapViewOfFile3)
helpviewer_keywords: ["MEM_LARGE_PAGES","MEM_REPLACE_PLACEHOLDER","MEM_RESERVE","MapViewOfFile3","MapViewOfFile3 function","base.mapviewoffile3","memoryapi/MapViewOfFile3"]
old-location: base\mapviewoffile3.htm
tech.root: base
ms.assetid: 585D7BA1-688F-4F24-8D8D-46A2FC137193
ms.date: 11/03/2024
ms.keywords: MEM_LARGE_PAGES, MEM_REPLACE_PLACEHOLDER, MEM_RESERVE, MapViewOfFile3, MapViewOfFile3 function, base.mapviewoffile3, memoryapi/MapViewOfFile3
req.header: memoryapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
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
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MapViewOfFile3
 - memoryapi/MapViewOfFile3
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
 - Kernel32.dll
 - onecore.lib
api_name:
 - MapViewOfFile3
---

# MapViewOfFile3 function


## -description

Maps a view of a file or a pagefile-backed section into the address space of the specified process.

## -parameters

### -param FileMapping [in]

A <b>HANDLE</b> to a section that is to be mapped into the address space of the specified process.

### -param Process [in]

A <b>HANDLE</b> to a process into which the section will be mapped.

### -param BaseAddress [in, optional]

The desired base address of the view (the address is rounded down to the nearest 64k boundary).

If this parameter is **NULL**, the system picks the base address.

If <i>BaseAddress</i> is not <b>NULL</b>, then any provided <a href="/windows/win32/api/winnt/ns-winnt-mem_address_requirements">MEM_ADDRESS_REQUIREMENTS</a> must consist of all zeroes.

### -param Offset [in]

The offset from the beginning of the section.

The offset must be 64k aligned or aligned to GetLargePageMinimum when MEM_LARGE_PAGES is used in AllocationType. Furthermore, the offset must be page-aligned to the underlying page size granted by VirtualAlloc2 when MEM_REPLACE_PLACEHOLDER is used in AllocationType.

### -param ViewSize [in]

The number of bytes to map. A value of zero (0) specifies that the entire section is to be mapped.

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
 Replaces a placeholder with a mapped view. Only data/pf-backed section views are supported (no images, physical memory, etc.). When you replace a placeholder, <i>BaseAddress</i> and <i>ViewSize</i> must exactly match those of the placeholder,
and any provided <a href="/windows/win32/api/winnt/ns-winnt-mem_address_requirements">MEM_ADDRESS_REQUIREMENTS</a> structure must consist of all zeroes.

After you replace a placeholder with a mapped view, to free that mapped view back to a placeholder, see the <i>UnmapFlags</i> parameter of <a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffileex">UnmapViewOfFileEx</a> and <a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile2">UnmapViewOfFile2</a>.

A placeholder is a type of reserved memory region.

The 64k alignment requirements on <i>Offset</i> and <i>BaseAddress</i> do not apply when this flag is specified.
</td>
</tr>
<tr>
<td width="40%"><a id="MEM_LARGE_PAGES"></a><a id="mem_large_pages"></a><dl>
<dt><b>MEM_LARGE_PAGES</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Maps a large page view. This flag specifies that the view should be mapped using <a href="/windows/desktop/Memory/large-page-support">large page support</a>. The size of the view must be a multiple of the size of a large page reported by the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-getlargepageminimum">GetLargePageMinimum</a> function, and the file-mapping object must have been created using the <b>SEC_LARGE_PAGES</b> option. If you provide a non-null value for the <i>BaseAddress</i> parameter, then the value must be a multiple of <b>GetLargePageMinimum</b>.

The 64k alignment requirements on <i>Offset</i> do not apply when this flag is specified.
</td>
</tr>
</table>

### -param PageProtection [in]

The desired page protection.

For file-mapping objects created with the <b>SEC_IMAGE</b> attribute, the <i>PageProtection</i> parameter has no effect, and should be set to any valid value such as <b>PAGE_READONLY</b>.

### -param ExtendedParameters [in, out, optional]

An optional pointer to one or more extended parameters of type <a href="/windows/win32/api/winnt/ns-winnt-mem_extended_parameter">MEM_EXTENDED_PARAMETER</a>. Each of those extended parameter values can itself have a <i>Type</i> field of either <b>MemExtendedParameterAddressRequirements</b> or <b>MemExtendedParameterNumaNode</b>. If no <b>MemExtendedParameterNumaNode</b> extended parameter is provided, then the behavior is the same as for the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>/<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> functions (that is, the preferred NUMA node for the physical pages is determined based on the ideal processor of the thread that first accesses the memory).

### -param ParameterCount [in]

The number of extended parameters pointed to by <i>ExtendedParameters</i>.

## -returns

Returns the base address of the mapped view, if successful. Otherwise, returns <b>NULL</b> and extended error status is available using <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This API helps support high-performance games, and server applications, which have particular requirements around managing their virtual address space. For example, mapping memory on top of a previously reserved region; this is useful for implementing an automatically wrapping ring buffer. And allocating memory with specific alignment; for example, to enable your application to commit large/huge page-mapped regions on demand.

Using this function for new allocations, you can:

- specify a range of virtual address space and a power-of-2 alignment restriction
- specify an arbitrary number of extended parameters
- specify a preferred NUMA node for the physical memory as an extended parameter
- specify a placeholder operation (specifically, replacement).

To specify the NUMA node, see the <i>ExtendedParameters</i> parameter.

#### Examples

For a code example, see Scenario 1 in <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc2">VirtualAlloc2</a>.

## -see-also

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc2">VirtualAlloc2</a>

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>


<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile2">MapViewOfFile2</a>

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffilenuma2">MapViewOfFileNuma2</a>
