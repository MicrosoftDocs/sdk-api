---
UID: NS:minidumpapiset._MINIDUMP_HANDLE_DATA_STREAM
title: MINIDUMP_HANDLE_DATA_STREAM (minidumpapiset.h)
description: Represents the header for a handle data stream.
helpviewer_keywords: ["*PMINIDUMP_HANDLE_DATA_STREAM","MINIDUMP_HANDLE_DATA_STREAM","MINIDUMP_HANDLE_DATA_STREAM structure","PMINIDUMP_HANDLE_DATA_STREAM","PMINIDUMP_HANDLE_DATA_STREAM structure pointer","_MINIDUMP_HANDLE_DATA_STREAM","_win32_minidump_handle_data_stream_str","base.minidump_handle_data_stream_str","minidumpapiset/MINIDUMP_HANDLE_DATA_STREAM","minidumpapiset/PMINIDUMP_HANDLE_DATA_STREAM"]
old-location: base\minidump_handle_data_stream_str.htm
tech.root: Debug
ms.assetid: 5674df6b-77e0-4bca-8349-8217388902ed
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_HANDLE_DATA_STREAM, MINIDUMP_HANDLE_DATA_STREAM, MINIDUMP_HANDLE_DATA_STREAM structure, PMINIDUMP_HANDLE_DATA_STREAM, PMINIDUMP_HANDLE_DATA_STREAM structure pointer, _MINIDUMP_HANDLE_DATA_STREAM, _win32_minidump_handle_data_stream_str, base.minidump_handle_data_stream_str, minidumpapiset/MINIDUMP_HANDLE_DATA_STREAM, minidumpapiset/PMINIDUMP_HANDLE_DATA_STREAM'
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
req.typenames: MINIDUMP_HANDLE_DATA_STREAM, *PMINIDUMP_HANDLE_DATA_STREAM
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_HANDLE_DATA_STREAM
 - minidumpapiset/_MINIDUMP_HANDLE_DATA_STREAM
 - PMINIDUMP_HANDLE_DATA_STREAM
 - minidumpapiset/PMINIDUMP_HANDLE_DATA_STREAM
 - MINIDUMP_HANDLE_DATA_STREAM
 - minidumpapiset/MINIDUMP_HANDLE_DATA_STREAM
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
 - MINIDUMP_HANDLE_DATA_STREAM
---

# MINIDUMP_HANDLE_DATA_STREAM structure


## -description

Represents the header for a handle data stream.

## -struct-fields

### -field SizeOfHeader

The size of the header information for the stream, in bytes. This value is <code>sizeof(MINIDUMP_HANDLE_DATA_STREAM)</code>.

### -field SizeOfDescriptor

The size of a descriptor in the stream, in bytes. This value is <code>sizeof(MINIDUMP_HANDLE_DESCRIPTOR)</code> or <code>sizeof(MINIDUMP_HANDLE_DESCRIPTOR_2)</code>.

### -field NumberOfDescriptors

The number of descriptors in the stream.

### -field Reserved

Reserved for future use; must be zero.

## -remarks

In this context, a data stream is a set of data in a minidump file. This header structure is followed by <b>NumberOfDescriptors</b>
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_descriptor">MINIDUMP_HANDLE_DESCRIPTOR</a> or <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_descriptor_2">MINIDUMP_HANDLE_DESCRIPTOR_2</a> structures.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_descriptor">MINIDUMP_HANDLE_DESCRIPTOR</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_descriptor">MINIDUMP_HANDLE_DESCRIPTOR_2</a>



<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>