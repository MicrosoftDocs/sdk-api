---
UID: NS:minidumpapiset._MINIDUMP_USER_STREAM_INFORMATION
title: MINIDUMP_USER_STREAM_INFORMATION (minidumpapiset.h)
author: windows-sdk-content
description: Contains a list of user data streams used by the MiniDumpWriteDump function.
old-location: base\minidump_user_stream_information_str.htm
tech.root: Debug
ms.assetid: 2a6b20ee-83cb-4000-b00a-61c4ab513205
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMINIDUMP_USER_STREAM_INFORMATION, MINIDUMP_USER_STREAM_INFORMATION, MINIDUMP_USER_STREAM_INFORMATION structure, PMINIDUMP_USER_STREAM_INFORMATION, PMINIDUMP_USER_STREAM_INFORMATION structure pointer, _MINIDUMP_USER_STREAM_INFORMATION, _win32_minidump_user_stream_information_str, base.minidump_user_stream_information_str, minidumpapiset/MINIDUMP_USER_STREAM_INFORMATION, minidumpapiset/PMINIDUMP_USER_STREAM_INFORMATION"
ms.topic: struct
f1_keywords: ["minidumpapiset/MINIDUMP_USER_STREAM_INFORMATION"]
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
 - MINIDUMP_USER_STREAM_INFORMATION
product: Windows
targetos: Windows
req.typenames: MINIDUMP_USER_STREAM_INFORMATION, *PMINIDUMP_USER_STREAM_INFORMATION
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# MINIDUMP_USER_STREAM_INFORMATION structure


## -description


Contains a list of user data streams used by the 
<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function.


## -struct-fields




### -field UserStreamCount

The number of user streams.


### -field UserStreamArray

An array of 
<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/ns-minidumpapiset-_minidump_user_stream">MINIDUMP_USER_STREAM</a> structures.


## -remarks



In this context, a data stream refers to a block of data within a minidump file.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/ns-minidumpapiset-_minidump_user_stream">MINIDUMP_USER_STREAM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a>
 

 

