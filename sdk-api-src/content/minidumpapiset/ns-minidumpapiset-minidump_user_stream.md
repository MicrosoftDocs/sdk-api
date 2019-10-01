---
UID: NS:minidumpapiset._MINIDUMP_USER_STREAM
title: MINIDUMP_USER_STREAM (minidumpapiset.h)
author: windows-sdk-content
description: Contains user-defined information stored in a data stream.
old-location: base\minidump_user_stream_str.htm
tech.root: Debug
ms.assetid: 43eae98c-fba3-43a4-97e6-8b81874e856e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_USER_STREAM, MINIDUMP_USER_STREAM, MINIDUMP_USER_STREAM structure, PMINIDUMP_USER_STREAM, PMINIDUMP_USER_STREAM structure pointer, _MINIDUMP_USER_STREAM, _win32_minidump_user_stream_str, base.minidump_user_stream_str, minidumpapiset/MINIDUMP_USER_STREAM, minidumpapiset/PMINIDUMP_USER_STREAM'
ms.topic: struct
f1_keywords:
- minidumpapiset/MINIDUMP_USER_STREAM
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- minidumpapiset.h
api_name:
- MINIDUMP_USER_STREAM
targetos: Windows
req.typenames: MINIDUMP_USER_STREAM, *PMINIDUMP_USER_STREAM
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# MINIDUMP_USER_STREAM structure


## -description


Contains user-defined information stored in a data stream.


## -struct-fields




### -field Type

The type of data stream. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>.


### -field BufferSize

The size of the user-defined data stream buffer, in bytes.


### -field Buffer

A pointer to a buffer that contains the user-defined data stream.


## -remarks



In this context, a data stream refers to a block of data within a minidump file.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>



<a href="https://docs.microsoft.com/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_user_stream_information">MINIDUMP_USER_STREAM_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>
 

 

