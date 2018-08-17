---
UID: NS:minidumpapiset._MINIDUMP_MEMORY_DESCRIPTOR
title: "_MINIDUMP_MEMORY_DESCRIPTOR"
author: windows-sdk-content
description: Describes a range of memory.
old-location: base\minidump_memory_descriptor_str.htm
old-project: debug
ms.assetid: 34c6de99-8ba5-4199-a382-3e3f7d02571f
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PMINIDUMP_MEMORY_DESCRIPTOR, MINIDUMP_MEMORY_DESCRIPTOR, MINIDUMP_MEMORY_DESCRIPTOR structure, MINIDUMP_MEMORY_DESCRIPTOR64, PMINIDUMP_MEMORY_DESCRIPTOR, PMINIDUMP_MEMORY_DESCRIPTOR structure pointer, _MINIDUMP_MEMORY_DESCRIPTOR, _win32_minidump_memory_descriptor_str, base.minidump_memory_descriptor_str, minidumpapiset/MINIDUMP_MEMORY_DESCRIPTOR, minidumpapiset/PMINIDUMP_MEMORY_DESCRIPTOR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h, Minidumpapiset.h
req.redist: DbgHelp.dll 5.1 or later
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
req.typenames: MINIDUMP_MEMORY_DESCRIPTOR, *PMINIDUMP_MEMORY_DESCRIPTOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_MEMORY_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_MEMORY_DESCRIPTOR structure


## -description


Describes a range of memory.


## -struct-fields




### -field StartOfMemoryRange

The starting address of the memory range.


### -field Memory

A 
<a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a> structure.


## -remarks



<b>MINIDUMP_MEMORY_DESCRIPTOR64</b> is used for full-memory minidumps where all of the raw memory is sequential at the end of the minidump. There is no need for individual relative virtual addresses (RVAs), because the RVA is the base RVA plus the sum of the preceding data blocks. The <b>MINIDUMP_MEMORY_DESCRIPTOR64</b> structure is defined as follows. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
typedef struct _MINIDUMP_MEMORY_DESCRIPTOR64 {
    ULONG64 StartOfMemoryRange;
    ULONG64 DataSize;
} MINIDUMP_MEMORY_DESCRIPTOR64, *PMINIDUMP_MEMORY_DESCRIPTOR64;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a>
 

 

