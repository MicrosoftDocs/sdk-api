---
UID: NS:minidumpapiset._MINIDUMP_MEMORY_LIST
title: "_MINIDUMP_MEMORY_LIST"
author: windows-sdk-content
description: Contains a list of memory ranges.
old-location: base\minidump_memory_list_str.htm
old-project: Debug
ms.assetid: 83a38831-fb90-495c-9f5d-90971849a7a0
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*PMINIDUMP_MEMORY_LIST, MINIDUMP_MEMORY64_LIST, MINIDUMP_MEMORY_LIST, MINIDUMP_MEMORY_LIST structure, PMINIDUMP_MEMORY_LIST, PMINIDUMP_MEMORY_LIST structure pointer, _MINIDUMP_MEMORY_LIST, _win32_minidump_memory_list_str, base.minidump_memory_list_str, minidumpapiset/MINIDUMP_MEMORY_LIST, minidumpapiset/PMINIDUMP_MEMORY_LIST"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h, Minidumpapiset.h
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
req.typenames: MINIDUMP_MEMORY_LIST, *PMINIDUMP_MEMORY_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	minidumpapiset.h
api_name:
-	MINIDUMP_MEMORY_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_MEMORY_LIST structure


## -description


Contains a list of memory ranges.


## -struct-fields




### -field NumberOfMemoryRanges

The number of structures in the <b>MemoryRanges</b> array.


### -field MemoryRanges

An array of 
<a href="https://msdn.microsoft.com/34c6de99-8ba5-4199-a382-3e3f7d02571f">MINIDUMP_MEMORY_DESCRIPTOR</a> structures.


## -remarks



The <b>MINIDUMP_MEMORY64_LIST</b> structure is defined as follows. It is used for full-memory minidumps.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
typedef struct _MINIDUMP_MEMORY64_LIST {
    ULONG64 NumberOfMemoryRanges;
    RVA64 BaseRva;
    MINIDUMP_MEMORY_DESCRIPTOR64 MemoryRanges [0];
} MINIDUMP_MEMORY64_LIST, *PMINIDUMP_MEMORY64_LIST;</pre>
</td>
</tr>
</table></span></div>
Note that <b>BaseRva</b> is the overall base RVA for the memory list. To locate the data for a particular descriptor, start at <b>BaseRva</b> and increment by the size of a descriptor until you reach the descriptor.




## -see-also




<a href="https://msdn.microsoft.com/34c6de99-8ba5-4199-a382-3e3f7d02571f">MINIDUMP_MEMORY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>
 

 

