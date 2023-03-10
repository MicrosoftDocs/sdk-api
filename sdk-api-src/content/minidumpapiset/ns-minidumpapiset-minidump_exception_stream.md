---
UID: NS:minidumpapiset.MINIDUMP_EXCEPTION_STREAM
title: MINIDUMP_EXCEPTION_STREAM (minidumpapiset.h)
description: Represents an exception information stream.
helpviewer_keywords: ["*PMINIDUMP_EXCEPTION_STREAM","MINIDUMP_EXCEPTION_STREAM","MINIDUMP_EXCEPTION_STREAM structure","PMINIDUMP_EXCEPTION_STREAM","PMINIDUMP_EXCEPTION_STREAM structure pointer","_win32_minidump_exception_stream_str","base.minidump_exception_stream_str","minidumpapiset/MINIDUMP_EXCEPTION_STREAM","minidumpapiset/PMINIDUMP_EXCEPTION_STREAM"]
old-location: base\minidump_exception_stream_str.htm
tech.root: Debug
ms.assetid: 2de717dc-a9ac-4b81-9fab-992f22da9a0d
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_EXCEPTION_STREAM, MINIDUMP_EXCEPTION_STREAM, MINIDUMP_EXCEPTION_STREAM structure, PMINIDUMP_EXCEPTION_STREAM, PMINIDUMP_EXCEPTION_STREAM structure pointer, _win32_minidump_exception_stream_str, base.minidump_exception_stream_str, minidumpapiset/MINIDUMP_EXCEPTION_STREAM, minidumpapiset/PMINIDUMP_EXCEPTION_STREAM'
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
req.typenames: MINIDUMP_EXCEPTION_STREAM, *PMINIDUMP_EXCEPTION_STREAM
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - MINIDUMP_EXCEPTION_STREAM
 - minidumpapiset/MINIDUMP_EXCEPTION_STREAM
 - PMINIDUMP_EXCEPTION_STREAM
 - minidumpapiset/PMINIDUMP_EXCEPTION_STREAM
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
 - MINIDUMP_EXCEPTION_STREAM
---

# MINIDUMP_EXCEPTION_STREAM structure


## -description

Represents an exception information stream.

## -struct-fields

### -field ThreadId

The identifier of the thread that caused the exception.

### -field __alignment

A variable for alignment.

### -field ExceptionRecord

A 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception">MINIDUMP_EXCEPTION</a> structure.

### -field ThreadContext

A 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_location_descriptor">MINIDUMP_LOCATION_DESCRIPTOR</a> structure.

## -remarks

In this context, a data stream is a set of data in a minidump file.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception">MINIDUMP_EXCEPTION</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_location_descriptor">MINIDUMP_LOCATION_DESCRIPTOR</a>



<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>