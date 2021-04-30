---
UID: NS:minidumpapiset._MINIDUMP_USER_STREAM
title: MINIDUMP_USER_STREAM (minidumpapiset.h)
description: Contains user-defined information stored in a data stream.
helpviewer_keywords: ["*PMINIDUMP_USER_STREAM","MINIDUMP_USER_STREAM","MINIDUMP_USER_STREAM structure","PMINIDUMP_USER_STREAM","PMINIDUMP_USER_STREAM structure pointer","_MINIDUMP_USER_STREAM","_win32_minidump_user_stream_str","base.minidump_user_stream_str","minidumpapiset/MINIDUMP_USER_STREAM","minidumpapiset/PMINIDUMP_USER_STREAM"]
old-location: base\minidump_user_stream_str.htm
tech.root: Debug
ms.assetid: 43eae98c-fba3-43a4-97e6-8b81874e856e
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_USER_STREAM, MINIDUMP_USER_STREAM, MINIDUMP_USER_STREAM structure, PMINIDUMP_USER_STREAM, PMINIDUMP_USER_STREAM structure pointer, _MINIDUMP_USER_STREAM, _win32_minidump_user_stream_str, base.minidump_user_stream_str, minidumpapiset/MINIDUMP_USER_STREAM, minidumpapiset/PMINIDUMP_USER_STREAM'
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
req.typenames: MINIDUMP_USER_STREAM, *PMINIDUMP_USER_STREAM
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_USER_STREAM
 - minidumpapiset/_MINIDUMP_USER_STREAM
 - PMINIDUMP_USER_STREAM
 - minidumpapiset/PMINIDUMP_USER_STREAM
 - MINIDUMP_USER_STREAM
 - minidumpapiset/MINIDUMP_USER_STREAM
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
 - MINIDUMP_USER_STREAM
---

# MINIDUMP_USER_STREAM structure


## -description

Contains user-defined information stored in a data stream.

## -struct-fields

### -field Type

The type of data stream. For more information, see 
<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>.

### -field BufferSize

The size of the user-defined data stream buffer, in bytes.

### -field Buffer

A pointer to a buffer that contains the user-defined data stream.

## -remarks

In this context, a data stream refers to a block of data within a minidump file.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_user_stream_information">MINIDUMP_USER_STREAM_INFORMATION</a>



<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>