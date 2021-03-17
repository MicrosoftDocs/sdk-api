---
UID: NS:minidumpapiset._MINIDUMP_FUNCTION_TABLE_STREAM
title: MINIDUMP_FUNCTION_TABLE_STREAM (minidumpapiset.h)
description: Represents the header for the function table stream.
helpviewer_keywords: ["*PMINIDUMP_FUNCTION_TABLE_STREAM","MINIDUMP_FUNCTION_TABLE_STREAM","MINIDUMP_FUNCTION_TABLE_STREAM structure","PMINIDUMP_FUNCTION_TABLE_STREAM","PMINIDUMP_FUNCTION_TABLE_STREAM structure pointer","_MINIDUMP_FUNCTION_TABLE_STREAM","_win32_minidump_function_table_stream_str","base.minidump_function_table_stream_str","minidumpapiset/MINIDUMP_FUNCTION_TABLE_STREAM","minidumpapiset/PMINIDUMP_FUNCTION_TABLE_STREAM"]
old-location: base\minidump_function_table_stream_str.htm
tech.root: Debug
ms.assetid: b2845799-acc9-4410-9059-45f7a8313e9f
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_FUNCTION_TABLE_STREAM, MINIDUMP_FUNCTION_TABLE_STREAM, MINIDUMP_FUNCTION_TABLE_STREAM structure, PMINIDUMP_FUNCTION_TABLE_STREAM, PMINIDUMP_FUNCTION_TABLE_STREAM structure pointer, _MINIDUMP_FUNCTION_TABLE_STREAM, _win32_minidump_function_table_stream_str, base.minidump_function_table_stream_str, minidumpapiset/MINIDUMP_FUNCTION_TABLE_STREAM, minidumpapiset/PMINIDUMP_FUNCTION_TABLE_STREAM'
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
req.typenames: MINIDUMP_FUNCTION_TABLE_STREAM, *PMINIDUMP_FUNCTION_TABLE_STREAM
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_FUNCTION_TABLE_STREAM
 - minidumpapiset/_MINIDUMP_FUNCTION_TABLE_STREAM
 - PMINIDUMP_FUNCTION_TABLE_STREAM
 - minidumpapiset/PMINIDUMP_FUNCTION_TABLE_STREAM
 - MINIDUMP_FUNCTION_TABLE_STREAM
 - minidumpapiset/MINIDUMP_FUNCTION_TABLE_STREAM
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
 - MINIDUMP_FUNCTION_TABLE_STREAM
---

# MINIDUMP_FUNCTION_TABLE_STREAM structure


## -description

Represents the header for the function table stream.

## -struct-fields

### -field SizeOfHeader

The size of header information for the stream, in bytes. This value is <code>sizeof(MINIDUMP_FUNCTION_TABLE_STREAM)</code>.

### -field SizeOfDescriptor

The size of a descriptor in the stream, in bytes. This value is <code>sizeof(MINIDUMP_FUNCTION_TABLE_DESCRIPTOR)</code>.

### -field SizeOfNativeDescriptor

The size of a raw system descriptor in the stream, in bytes. This value depends on the particular platform and system version on which the minidump was generated.

### -field SizeOfFunctionEntry

The size of a raw system function table entry, in bytes. This value depends on the particular platform and system version on which the minidump was generated.

### -field NumberOfDescriptors

The number of descriptors in the stream.

### -field SizeOfAlignPad

The size of alignment padding that follows the header, in bytes.

## -remarks

In this context, a data stream is a set of data in a minidump file. This header structure is followed by <b>NumberOfDescriptors</b> function tables. For each function table there is a 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_function_table_descriptor">MINIDUMP_FUNCTION_TABLE_DESCRIPTOR</a> structure, then the raw system descriptor for the table, then the raw system function entry data. If necessary, alignment padding is placed between tables to properly align the initial structures.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_function_table_descriptor">MINIDUMP_FUNCTION_TABLE_DESCRIPTOR</a>



<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>