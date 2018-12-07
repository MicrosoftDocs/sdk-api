---
UID: NS:minidumpapiset._MINIDUMP_USER_STREAM
title: "_MINIDUMP_USER_STREAM"
author: windows-sdk-content
description: Contains user-defined information stored in a data stream.
old-location: base\minidump_user_stream_str.htm
tech.root: debug
ms.assetid: 43eae98c-fba3-43a4-97e6-8b81874e856e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMINIDUMP_USER_STREAM, MINIDUMP_USER_STREAM, MINIDUMP_USER_STREAM structure, PMINIDUMP_USER_STREAM, PMINIDUMP_USER_STREAM structure pointer, _MINIDUMP_USER_STREAM, _win32_minidump_user_stream_str, base.minidump_user_stream_str, minidumpapiset/MINIDUMP_USER_STREAM, minidumpapiset/PMINIDUMP_USER_STREAM"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: MINIDUMP_USER_STREAM, *PMINIDUMP_USER_STREAM
req.redist: DbgHelp.dll 5.1 or later
---

# _MINIDUMP_USER_STREAM structure


## -description


Contains user-defined information stored in a data stream.


## -struct-fields




### -field Type

The type of data stream. For more information, see 
<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>.


### -field BufferSize

The size of the user-defined data stream buffer, in bytes.


### -field Buffer

A pointer to a buffer that contains the user-defined data stream.


## -remarks



In this context, a data stream refers to a block of data within a minidump file.




## -see-also




<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>



<a href="https://msdn.microsoft.com/2a6b20ee-83cb-4000-b00a-61c4ab513205">MINIDUMP_USER_STREAM_INFORMATION</a>



<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a>
 

 

