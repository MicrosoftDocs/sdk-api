---
UID: NS:winnt._MEMORY_BASIC_INFORMATION
title: MEMORY_BASIC_INFORMATION (winnt.h)
description: Contains information about a range of pages in the virtual address space of a process.
helpviewer_keywords: ["*PMEMORY_BASIC_INFORMATION","MEMORY_BASIC_INFORMATION","MEMORY_BASIC_INFORMATION structure","MEM_COMMIT","MEM_FREE","MEM_IMAGE","MEM_MAPPED","MEM_PRIVATE","MEM_RESERVE","PMEMORY_BASIC_INFORMATION","PMEMORY_BASIC_INFORMATION structure pointer","_MEMORY_BASIC_INFORMATION","_win32_memory_basic_information_str","base.memory_basic_information_str","winnt/MEMORY_BASIC_INFORMATION","winnt/PMEMORY_BASIC_INFORMATION"]
old-location: base\memory_basic_information_str.htm
tech.root: base
ms.assetid: dc3fa48e-0986-49cc-88a9-ff8179fbe5f0
ms.date: 12/05/2018
ms.keywords: '*PMEMORY_BASIC_INFORMATION, MEMORY_BASIC_INFORMATION, MEMORY_BASIC_INFORMATION structure, MEM_COMMIT, MEM_FREE, MEM_IMAGE, MEM_MAPPED, MEM_PRIVATE, MEM_RESERVE, PMEMORY_BASIC_INFORMATION, PMEMORY_BASIC_INFORMATION structure pointer, _MEMORY_BASIC_INFORMATION, _win32_memory_basic_information_str, base.memory_basic_information_str, winnt/MEMORY_BASIC_INFORMATION, winnt/PMEMORY_BASIC_INFORMATION'
req.header: winnt.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MEMORY_BASIC_INFORMATION, *PMEMORY_BASIC_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MEMORY_BASIC_INFORMATION
 - winnt/_MEMORY_BASIC_INFORMATION
 - PMEMORY_BASIC_INFORMATION
 - winnt/PMEMORY_BASIC_INFORMATION
 - MEMORY_BASIC_INFORMATION
 - winnt/MEMORY_BASIC_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - MEMORY_BASIC_INFORMATION
---

# MEMORY_BASIC_INFORMATION structure


## -description

Contains information about a range of pages in the virtual address space of a process. The 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualquery">VirtualQuery</a> and 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex">VirtualQueryEx</a> functions use this structure.

## -struct-fields

### -field BaseAddress

A pointer to the base address of the region of pages.

### -field AllocationBase

A pointer to the base address of a range of pages allocated by the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function. The page pointed to by the <b>BaseAddress</b> member is contained within this allocation range.

### -field AllocationProtect

The memory protection option when the region was initially allocated. This member can be one of the 
<a href="/windows/desktop/Memory/memory-protection-constants">memory protection constants</a> or 0 if the caller does not have access.

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

## -remarks

To enable a debugger to debug a target that is running on a different architecture (32-bit versus 64-bit), use one of the explicit forms of this structure.


```cpp
typedef struct _MEMORY_BASIC_INFORMATION32 {
    DWORD BaseAddress;
    DWORD AllocationBase;
    DWORD AllocationProtect;
    DWORD RegionSize;
    DWORD State;
    DWORD Protect;
    DWORD Type;
} MEMORY_BASIC_INFORMATION32, *PMEMORY_BASIC_INFORMATION32;

typedef struct DECLSPEC_ALIGN(16) _MEMORY_BASIC_INFORMATION64 {
    ULONGLONG BaseAddress;
    ULONGLONG AllocationBase;
    DWORD     AllocationProtect;
    DWORD     __alignment1;
    ULONGLONG RegionSize;
    DWORD     State;
    DWORD     Protect;
    DWORD     Type;
    DWORD     __alignment2;
} MEMORY_BASIC_INFORMATION64, *PMEMORY_BASIC_INFORMATION64;
```

## -see-also

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualquery">VirtualQuery</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex">VirtualQueryEx</a>