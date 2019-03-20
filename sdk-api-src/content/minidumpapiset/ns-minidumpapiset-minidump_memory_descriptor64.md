---
UID: NS:minidumpapiset._MINIDUMP_MEMORY_DESCRIPTOR64
title: MINIDUMP_MEMORY_DESCRIPTOR64 (minidumpapiset.h)
author: windows-sdk-content
description: Describes a range of memory.
old-location: base\minidump_memory_descriptor_str.htm
tech.root: Debug
ms.assetid: 34c6de99-8ba5-4199-a382-3e3f7d02571f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMINIDUMP_MEMORY_DESCRIPTOR64, MINIDUMP_MEMORY_DESCRIPTOR, MINIDUMP_MEMORY_DESCRIPTOR structure, MINIDUMP_MEMORY_DESCRIPTOR64, PMINIDUMP_MEMORY_DESCRIPTOR, PMINIDUMP_MEMORY_DESCRIPTOR structure pointer, _MINIDUMP_MEMORY_DESCRIPTOR, _win32_minidump_memory_descriptor_str, base.minidump_memory_descriptor_str, minidumpapiset/MINIDUMP_MEMORY_DESCRIPTOR, minidumpapiset/PMINIDUMP_MEMORY_DESCRIPTOR"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: MINIDUMP_MEMORY_DESCRIPTOR64, *PMINIDUMP_MEMORY_DESCRIPTOR64
req.redist: DbgHelp.dll 5.1 or later
---

# MINIDUMP_MEMORY_DESCRIPTOR64 structure


## -description


Describes a range of memory.


## -struct-fields




### -field StartOfMemoryRange

The starting address of the memory range.


### -field DataSize

 




#### - Memory

A 
<a href="https://msdn.microsoft.com/en-us/library/ms680383(v=VS.85).aspx">MINIDUMP_LOCATION_DESCRIPTOR</a> structure.


## -remarks



<b>MINIDUMP_MEMORY_DESCRIPTOR64</b> is used for full-memory minidumps where all of the raw memory is sequential at the end of the minidump. There is no need for individual relative virtual addresses (RVAs), because the RVA is the base RVA plus the sum of the preceding data blocks. The <b>MINIDUMP_MEMORY_DESCRIPTOR64</b> structure is defined as follows. 


```cpp

typedef struct _MINIDUMP_MEMORY_DESCRIPTOR64 {
    ULONG64 StartOfMemoryRange;
    ULONG64 DataSize;
} MINIDUMP_MEMORY_DESCRIPTOR64, *PMINIDUMP_MEMORY_DESCRIPTOR64;
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680383(v=VS.85).aspx">MINIDUMP_LOCATION_DESCRIPTOR</a>
 

 

