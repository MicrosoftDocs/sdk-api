---
UID: NS:minidumpapiset._MINIDUMP_DIRECTORY
title: MINIDUMP_DIRECTORY (minidumpapiset.h)
description: Contains the information needed to access a specific data stream in a minidump file.helpviewer_keywords: ["*PMINIDUMP_DIRECTORY","MINIDUMP_DIRECTORY","MINIDUMP_DIRECTORY structure","PMINIDUMP_DIRECTORY","PMINIDUMP_DIRECTORY structure pointer","_MINIDUMP_DIRECTORY","_win32_minidump_directory_str","base.minidump_directory_str","minidumpapiset/MINIDUMP_DIRECTORY","minidumpapiset/PMINIDUMP_DIRECTORY"]
old-location: base\minidump_directory_str.htm
tech.root: Debug
ms.assetid: 1262c218-5351-4fea-9d35-4654da7c5e44
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_DIRECTORY, MINIDUMP_DIRECTORY, MINIDUMP_DIRECTORY structure, PMINIDUMP_DIRECTORY, PMINIDUMP_DIRECTORY structure pointer, _MINIDUMP_DIRECTORY, _win32_minidump_directory_str, base.minidump_directory_str, minidumpapiset/MINIDUMP_DIRECTORY, minidumpapiset/PMINIDUMP_DIRECTORY'
f1_keywords:
- minidumpapiset/MINIDUMP_DIRECTORY
dev_langs:
- c++
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
- MINIDUMP_DIRECTORY
targetos: Windows
req.typenames: MINIDUMP_DIRECTORY, *PMINIDUMP_DIRECTORY
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# MINIDUMP_DIRECTORY structure


## -description


Contains the information needed to access a specific data stream in a minidump file.


## -struct-fields




### -field StreamType

The type of data stream. This member can be one of the values in the 
<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a> enumeration.


### -field Location

A 
<a href="https://docs.microsoft.com/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_location_descriptor">MINIDUMP_LOCATION_DESCRIPTOR</a> structure that specifies the location of the data stream.


## -remarks



In this context, a data stream is a block of data within a minidump file.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_location_descriptor">MINIDUMP_LOCATION_DESCRIPTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream">MiniDumpReadDumpStream</a>
 

 

