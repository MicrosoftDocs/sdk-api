---
UID: NS:minidumpapiset._MINIDUMP_MEMORY_INFO
title: MINIDUMP_MEMORY_INFO (minidumpapiset.h)
description: Describes a region of memory.
helpviewer_keywords: ["*PMINIDUMP_MEMORY_INFO","MEM_COMMIT","MEM_FREE","MEM_IMAGE","MEM_MAPPED","MEM_PRIVATE","MEM_RESERVE","MINIDUMP_MEMORY_INFO","MINIDUMP_MEMORY_INFO structure","PMINIDUMP_MEMORY_INFO","PMINIDUMP_MEMORY_INFO structure pointer","_MINIDUMP_MEMORY_INFO","base.minidump_memory_info_str","minidumpapiset/MINIDUMP_MEMORY_INFO","minidumpapiset/PMINIDUMP_MEMORY_INFO"]
old-location: base\minidump_memory_info_str.htm
tech.root: Debug
ms.assetid: e9a797b9-5cad-48c0-bb33-ca9c13de8239
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_MEMORY_INFO, MEM_COMMIT, MEM_FREE, MEM_IMAGE, MEM_MAPPED, MEM_PRIVATE, MEM_RESERVE, MINIDUMP_MEMORY_INFO, MINIDUMP_MEMORY_INFO structure, PMINIDUMP_MEMORY_INFO, PMINIDUMP_MEMORY_INFO structure pointer, _MINIDUMP_MEMORY_INFO, base.minidump_memory_info_str, minidumpapiset/MINIDUMP_MEMORY_INFO, minidumpapiset/PMINIDUMP_MEMORY_INFO'
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MINIDUMP_MEMORY_INFO, *PMINIDUMP_MEMORY_INFO
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_MEMORY_INFO
 - minidumpapiset/_MINIDUMP_MEMORY_INFO
 - PMINIDUMP_MEMORY_INFO
 - minidumpapiset/PMINIDUMP_MEMORY_INFO
 - MINIDUMP_MEMORY_INFO
 - minidumpapiset/MINIDUMP_MEMORY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_MEMORY_INFO
---

# MINIDUMP_MEMORY_INFO structure


## -description

Describes a region of memory.

## -struct-fields

### -field BaseAddress

The base address of the region of pages.

### -field AllocationBase

The base address of a range of pages in this region. The page is contained within this memory region.

### -field AllocationProtect

The memory protection when the region was initially allocated. This member can be one of the 
<a href="/windows/desktop/Memory/memory-protection">memory protection</a> options, along with PAGE_GUARD or PAGE_NOCACHE, as needed.

### -field __alignment1

A variable for alignment.

### -field RegionSize

The size of the region beginning at the base address in which all pages have identical attributes, in bytes.

### -field State

The state of the pages in the region. This member can be one of the following values. 



<table>
<tr>
<th>State</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEM_COMMIT"></a><a id="mem_commit"></a><dl>
<dt><b>MEM_COMMIT</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Indicates committed pages for which physical storage has been allocated, either in memory or in the paging file on disk.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_FREE"></a><a id="mem_free"></a><dl>
<dt><b>MEM_FREE</b></dt>
<dt>0x10000</dt>
</dl>
</td>
<td width="60%">
Indicates free pages not accessible to the calling process and available to be allocated. For free pages, the information in the <b>AllocationBase</b>, <b>AllocationProtect</b>, <b>Protect</b>, and <b>Type</b> members is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_RESERVE"></a><a id="mem_reserve"></a><dl>
<dt><b>MEM_RESERVE</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
Indicates reserved pages where a range of the process's virtual address space is reserved without any physical storage being allocated. For reserved pages, the information in the <b>Protect</b> member is undefined.

</td>
</tr>
</table>

### -field Protect

The access protection of the pages in the region. This member is one of the values listed for the <b>AllocationProtect</b> member.

### -field Type

The type of pages in the region. The following types are defined. 



<table>
<tr>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEM_IMAGE"></a><a id="mem_image"></a><dl>
<dt><b>MEM_IMAGE</b></dt>
<dt>0x1000000</dt>
</dl>
</td>
<td width="60%">
Indicates that the memory pages within the region are mapped into the view of an image section.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_MAPPED"></a><a id="mem_mapped"></a><dl>
<dt><b>MEM_MAPPED</b></dt>
<dt>0x40000</dt>
</dl>
</td>
<td width="60%">
Indicates that the memory pages within the region are mapped into the view of a section.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_PRIVATE"></a><a id="mem_private"></a><dl>
<dt><b>MEM_PRIVATE</b></dt>
<dt>0x20000</dt>
</dl>
</td>
<td width="60%">
Indicates that the memory pages within the region are private (that is, not shared by other processes).

</td>
</tr>
</table>

### -field __alignment2

A variable for alignment.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory_info_list">MINIDUMP_MEMORY_INFO_LIST</a>