---
UID: NS:minidumpapiset._MINIDUMP_USER_STREAM_INFORMATION
title: "_MINIDUMP_USER_STREAM_INFORMATION"
author: windows-sdk-content
description: Contains a list of user data streams used by the MiniDumpWriteDump function.
old-location: base\minidump_user_stream_information_str.htm
old-project: debug
ms.assetid: 2a6b20ee-83cb-4000-b00a-61c4ab513205
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: "*PMINIDUMP_USER_STREAM_INFORMATION, MINIDUMP_USER_STREAM_INFORMATION, MINIDUMP_USER_STREAM_INFORMATION structure, PMINIDUMP_USER_STREAM_INFORMATION, PMINIDUMP_USER_STREAM_INFORMATION structure pointer, _MINIDUMP_USER_STREAM_INFORMATION, _win32_minidump_user_stream_information_str, base.minidump_user_stream_information_str, minidumpapiset/MINIDUMP_USER_STREAM_INFORMATION, minidumpapiset/PMINIDUMP_USER_STREAM_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.redist: DbgHelp.dll 5.1 or later
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
tech.root: 
req.typenames: MINIDUMP_USER_STREAM_INFORMATION, *PMINIDUMP_USER_STREAM_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_USER_STREAM_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_USER_STREAM_INFORMATION structure


## -description


Contains a list of user data streams used by the 
<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a> function.


## -struct-fields




### -field UserStreamCount

The number of user streams.


### -field UserStreamArray

An array of 
<a href="https://msdn.microsoft.com/43eae98c-fba3-43a4-97e6-8b81874e856e">MINIDUMP_USER_STREAM</a> structures.


## -remarks



In this context, a data stream refers to a block of data within a minidump file.




## -see-also




<a href="https://msdn.microsoft.com/43eae98c-fba3-43a4-97e6-8b81874e856e">MINIDUMP_USER_STREAM</a>



<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a>
 

 

