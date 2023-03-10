---
UID: NS:minidumpapiset._MINIDUMP_MEMORY_DESCRIPTOR
title: MINIDUMP_MEMORY_DESCRIPTOR (minidumpapiset.h)
description: Describes a range of memory. (MINIDUMP_MEMORY_DESCRIPTOR)
helpviewer_keywords: ["*PMINIDUMP_MEMORY_DESCRIPTOR","MINIDUMP_MEMORY_DESCRIPTOR","MINIDUMP_MEMORY_DESCRIPTOR structure","MINIDUMP_MEMORY_DESCRIPTOR64","PMINIDUMP_MEMORY_DESCRIPTOR","PMINIDUMP_MEMORY_DESCRIPTOR structure pointer","_MINIDUMP_MEMORY_DESCRIPTOR","_win32_minidump_memory_descriptor_str","base.minidump_memory_descriptor_str","minidumpapiset/MINIDUMP_MEMORY_DESCRIPTOR","minidumpapiset/PMINIDUMP_MEMORY_DESCRIPTOR"]
old-location: base\minidump_memory_descriptor_str.htm
tech.root: Debug
ms.assetid: 34c6de99-8ba5-4199-a382-3e3f7d02571f
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_MEMORY_DESCRIPTOR, MINIDUMP_MEMORY_DESCRIPTOR, MINIDUMP_MEMORY_DESCRIPTOR structure, MINIDUMP_MEMORY_DESCRIPTOR64, PMINIDUMP_MEMORY_DESCRIPTOR, PMINIDUMP_MEMORY_DESCRIPTOR structure pointer, _MINIDUMP_MEMORY_DESCRIPTOR, _win32_minidump_memory_descriptor_str, base.minidump_memory_descriptor_str, minidumpapiset/MINIDUMP_MEMORY_DESCRIPTOR, minidumpapiset/PMINIDUMP_MEMORY_DESCRIPTOR'
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
targetos: Windows
req.typenames: MINIDUMP_MEMORY_DESCRIPTOR, *PMINIDUMP_MEMORY_DESCRIPTOR
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_MEMORY_DESCRIPTOR
 - minidumpapiset/_MINIDUMP_MEMORY_DESCRIPTOR
 - PMINIDUMP_MEMORY_DESCRIPTOR
 - minidumpapiset/PMINIDUMP_MEMORY_DESCRIPTOR
 - MINIDUMP_MEMORY_DESCRIPTOR
 - minidumpapiset/MINIDUMP_MEMORY_DESCRIPTOR
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
 - MINIDUMP_MEMORY_DESCRIPTOR
---

# MINIDUMP_MEMORY_DESCRIPTOR structure


## -description

Describes a range of memory.

## -struct-fields

### -field StartOfMemoryRange

The starting address of the memory range.

### -field Memory

A 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_location_descriptor">MINIDUMP_LOCATION_DESCRIPTOR</a> structure.

## -remarks

<b>MINIDUMP_MEMORY_DESCRIPTOR64</b> is used for full-memory minidumps where all of the raw memory is sequential at the end of the minidump. There is no need for individual relative virtual addresses (RVAs), because the RVA is the base RVA plus the sum of the preceding data blocks. The <b>MINIDUMP_MEMORY_DESCRIPTOR64</b> structure is defined as follows. 


```cpp

typedef struct _MINIDUMP_MEMORY_DESCRIPTOR64 {
    ULONG64 StartOfMemoryRange;
    ULONG64 DataSize;
} MINIDUMP_MEMORY_DESCRIPTOR64, *PMINIDUMP_MEMORY_DESCRIPTOR64;
```

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_location_descriptor">MINIDUMP_LOCATION_DESCRIPTOR</a>

