---
UID: NS:minidumpapiset._MINIDUMP_LOCATION_DESCRIPTOR64
title: MINIDUMP_LOCATION_DESCRIPTOR64 (minidumpapiset.h)
description: Contains information describing the location of a data stream within a minidump file.M
helpviewer_keywords: ["MINIDUMP_LOCATION_DESCRIPTOR","MINIDUMP_LOCATION_DESCRIPTOR structure","MINIDUMP_LOCATION_DESCRIPTOR64","_MINIDUMP_LOCATION_DESCRIPTOR","_win32_minidump_location_descriptor_str","base.minidump_location_descriptor_str","minidumpapiset/MINIDUMP_LOCATION_DESCRIPTOR"]
old-location: base\minidump_location_descriptor_str.htm
tech.root: Debug
ms.assetid: aef17239-9b56-4d49-8347-610270f8612b
ms.date: 12/05/2018
ms.keywords: MINIDUMP_LOCATION_DESCRIPTOR, MINIDUMP_LOCATION_DESCRIPTOR structure, MINIDUMP_LOCATION_DESCRIPTOR64, _MINIDUMP_LOCATION_DESCRIPTOR, _win32_minidump_location_descriptor_str, base.minidump_location_descriptor_str, minidumpapiset/MINIDUMP_LOCATION_DESCRIPTOR
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
req.typenames: MINIDUMP_LOCATION_DESCRIPTOR64
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_LOCATION_DESCRIPTOR64
 - minidumpapiset/_MINIDUMP_LOCATION_DESCRIPTOR64
 - MINIDUMP_LOCATION_DESCRIPTOR64
 - minidumpapiset/MINIDUMP_LOCATION_DESCRIPTOR64
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
 - MINIDUMP_LOCATION_DESCRIPTOR
---

# MINIDUMP_LOCATION_DESCRIPTOR64 structure


## -description

Contains information describing the location of a data stream within a minidump file.

## -struct-fields

### -field DataSize

The size of the data stream, in bytes.

### -field Rva

The relative virtual address (RVA) of the data. This is the byte offset of the data stream from the beginning of the minidump file.

## -remarks

In this context, a data stream refers to a block of data within a minidump file.

This structure uses 32-bit locations for RVAs in the first 4GB and 64-bit locations are used for larger RVAs. The <b>MINIDUMP_LOCATION_DESCRIPTOR64</b> structure is defined as follows.


```cpp

typedef struct _MINIDUMP_LOCATION_DESCRIPTOR64 {
  ULONG64 DataSize;
  RVA64 Rva;
} MINIDUMP_LOCATION_DESCRIPTOR64;
```

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_directory">MINIDUMP_DIRECTORY</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_stream">MINIDUMP_EXCEPTION_STREAM</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory_descriptor">MINIDUMP_MEMORY_DESCRIPTOR</a>
