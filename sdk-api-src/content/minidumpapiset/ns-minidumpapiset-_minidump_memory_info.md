---
UID: NS:minidumpapiset._MINIDUMP_MEMORY_INFO
title: "_MINIDUMP_MEMORY_INFO"
author: windows-sdk-content
description: Describes a region of memory.
old-location: base\minidump_memory_info_str.htm
old-project: debug
ms.assetid: e9a797b9-5cad-48c0-bb33-ca9c13de8239
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMINIDUMP_MEMORY_INFO, MEM_COMMIT, MEM_FREE, MEM_IMAGE, MEM_MAPPED, MEM_PRIVATE, MEM_RESERVE, MINIDUMP_MEMORY_INFO, MINIDUMP_MEMORY_INFO structure, PMINIDUMP_MEMORY_INFO, PMINIDUMP_MEMORY_INFO structure pointer, _MINIDUMP_MEMORY_INFO, base.minidump_memory_info_str, minidumpapiset/MINIDUMP_MEMORY_INFO, minidumpapiset/PMINIDUMP_MEMORY_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MINIDUMP_MEMORY_INFO, *PMINIDUMP_MEMORY_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_MEMORY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_MEMORY_INFO structure


## -description


Describes a region of memory.


## -struct-fields




### -field BaseAddress

The base address of the region of pages.


### -field AllocationBase

The base address of a range of pages in this region. The page is contained within this memory region.


### -field AllocationProtect

The memory protection when the region was initially allocated. This member can be one of the 
<a href="https://msdn.microsoft.com/70ded07a-7be6-4189-a1ae-281917f42a1e">memory protection</a> options, along with PAGE_GUARD or PAGE_NOCACHE, as needed.


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




<a href="https://msdn.microsoft.com/c1c9a79b-a35a-47e8-be4c-10b3c4ace937">MINIDUMP_MEMORY_INFO_LIST</a>
 

 

