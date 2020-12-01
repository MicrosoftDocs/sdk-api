---
UID: NS:minidumpapiset._MINIDUMP_FUNCTION_TABLE_DESCRIPTOR
title: MINIDUMP_FUNCTION_TABLE_DESCRIPTOR (minidumpapiset.h)
description: Represents a function table stream.
helpviewer_keywords: ["*PMINIDUMP_FUNCTION_TABLE_DESCRIPTOR","MINIDUMP_FUNCTION_TABLE_DESCRIPTOR","MINIDUMP_FUNCTION_TABLE_DESCRIPTOR structure","PMINIDUMP_FUNCTION_TABLE_DESCRIPTOR","PMINIDUMP_FUNCTION_TABLE_DESCRIPTOR structure pointer","_MINIDUMP_FUNCTION_TABLE_DESCRIPTOR","_win32_minidump_function_table_descriptor_str","base.minidump_function_table_descriptor_str","minidumpapiset/MINIDUMP_FUNCTION_TABLE_DESCRIPTOR","minidumpapiset/PMINIDUMP_FUNCTION_TABLE_DESCRIPTOR"]
old-location: base\minidump_function_table_descriptor_str.htm
tech.root: Debug
ms.assetid: 284435dc-3443-4b26-9c13-ce9567482628
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_FUNCTION_TABLE_DESCRIPTOR, MINIDUMP_FUNCTION_TABLE_DESCRIPTOR, MINIDUMP_FUNCTION_TABLE_DESCRIPTOR structure, PMINIDUMP_FUNCTION_TABLE_DESCRIPTOR, PMINIDUMP_FUNCTION_TABLE_DESCRIPTOR structure pointer, _MINIDUMP_FUNCTION_TABLE_DESCRIPTOR, _win32_minidump_function_table_descriptor_str, base.minidump_function_table_descriptor_str, minidumpapiset/MINIDUMP_FUNCTION_TABLE_DESCRIPTOR, minidumpapiset/PMINIDUMP_FUNCTION_TABLE_DESCRIPTOR'
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
req.typenames: MINIDUMP_FUNCTION_TABLE_DESCRIPTOR, *PMINIDUMP_FUNCTION_TABLE_DESCRIPTOR
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_FUNCTION_TABLE_DESCRIPTOR
 - minidumpapiset/_MINIDUMP_FUNCTION_TABLE_DESCRIPTOR
 - PMINIDUMP_FUNCTION_TABLE_DESCRIPTOR
 - minidumpapiset/PMINIDUMP_FUNCTION_TABLE_DESCRIPTOR
 - MINIDUMP_FUNCTION_TABLE_DESCRIPTOR
 - minidumpapiset/MINIDUMP_FUNCTION_TABLE_DESCRIPTOR
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
 - MINIDUMP_FUNCTION_TABLE_DESCRIPTOR
---

# MINIDUMP_FUNCTION_TABLE_DESCRIPTOR structure


## -description

Represents a function table stream.

## -struct-fields

### -field MinimumAddress

The minimum address of functions described by the table.

### -field MaximumAddress

The maximum address of functions described by the table.

### -field BaseAddress

The base address to use when computing full virtual addresses from relative virtual addresses in function entries.

### -field EntryCount

The number of entries in the function table.

### -field SizeOfAlignPad

The size of alignment padding that follows the function entry data, in bytes. The function entry data in the stream is guaranteed to be aligned appropriately for access to the data members. If a minidump is directly mapped in memory, it is always possible to directly reference structure members in the stream.

## -remarks

The first descriptor in the function table stream follows the header, 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_function_table_stream">MINIDUMP_FUNCTION_TABLE_STREAM</a>. The generic descriptor is followed by a native system descriptor, then by <b>EntryCount</b> native system function entry structures.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_function_table_stream">MINIDUMP_FUNCTION_TABLE_STREAM</a>

