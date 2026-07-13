---
UID: NS:minidumpapiset._MINIDUMP_MEMORY64_LIST
title: MINIDUMP_MEMORY64_LIST (minidumpapiset.h)
description: Contains a list of memory ranges.M
helpviewer_keywords: ["*PMINIDUMP_MEMORY64_LIST","MINIDUMP_MEMORY64_LIST","MINIDUMP_MEMORY_LIST","MINIDUMP_MEMORY_LIST structure","PMINIDUMP_MEMORY_LIST","PMINIDUMP_MEMORY_LIST structure pointer","_MINIDUMP_MEMORY_LIST","_win32_minidump_memory_list_str","base.minidump_memory_list_str","minidumpapiset/MINIDUMP_MEMORY_LIST","minidumpapiset/PMINIDUMP_MEMORY_LIST"]
old-location: base\minidump_memory_list_str.htm
tech.root: Debug
ms.assetid: 83a38831-fb90-495c-9f5d-90971849a7a0
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_MEMORY64_LIST, MINIDUMP_MEMORY64_LIST, MINIDUMP_MEMORY_LIST, MINIDUMP_MEMORY_LIST structure, PMINIDUMP_MEMORY_LIST, PMINIDUMP_MEMORY_LIST structure pointer, _MINIDUMP_MEMORY_LIST, _win32_minidump_memory_list_str, base.minidump_memory_list_str, minidumpapiset/MINIDUMP_MEMORY_LIST, minidumpapiset/PMINIDUMP_MEMORY_LIST'
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
req.typenames: MINIDUMP_MEMORY64_LIST, *PMINIDUMP_MEMORY64_LIST
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_MEMORY64_LIST
 - minidumpapiset/_MINIDUMP_MEMORY64_LIST
 - PMINIDUMP_MEMORY64_LIST
 - minidumpapiset/PMINIDUMP_MEMORY64_LIST
 - MINIDUMP_MEMORY64_LIST
 - minidumpapiset/MINIDUMP_MEMORY64_LIST
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
 - MINIDUMP_MEMORY_LIST
---

# MINIDUMP_MEMORY64_LIST structure


## -description

Contains a list of memory ranges.

## -struct-fields

### -field NumberOfMemoryRanges

The number of structures in the <b>MemoryRanges</b> array.

### -field BaseRva

### -field MemoryRanges

An array of 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory_descriptor">MINIDUMP_MEMORY_DESCRIPTOR</a> structures.

## -remarks

The <b>MINIDUMP_MEMORY64_LIST</b> structure is defined as follows. It is used for full-memory minidumps.


```cpp

typedef struct _MINIDUMP_MEMORY64_LIST {
    ULONG64 NumberOfMemoryRanges;
    RVA64 BaseRva;
    MINIDUMP_MEMORY_DESCRIPTOR64 MemoryRanges [0];
} MINIDUMP_MEMORY64_LIST, *PMINIDUMP_MEMORY64_LIST;
```


Note that <b>BaseRva</b> is the overall base RVA for the memory list. To locate the data for a particular descriptor, start at <b>BaseRva</b> and increment by the size of a descriptor until you reach the descriptor.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory_descriptor">MINIDUMP_MEMORY_DESCRIPTOR</a>



<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>
