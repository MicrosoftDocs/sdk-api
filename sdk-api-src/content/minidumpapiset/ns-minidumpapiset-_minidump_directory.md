---
UID: NS:minidumpapiset._MINIDUMP_DIRECTORY
title: "_MINIDUMP_DIRECTORY"
author: windows-sdk-content
description: Contains the information needed to access a specific data stream in a minidump file.
old-location: base\minidump_directory_str.htm
tech.root: debug
ms.assetid: 1262c218-5351-4fea-9d35-4654da7c5e44
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PMINIDUMP_DIRECTORY, MINIDUMP_DIRECTORY, MINIDUMP_DIRECTORY structure, PMINIDUMP_DIRECTORY, PMINIDUMP_DIRECTORY structure pointer, _MINIDUMP_DIRECTORY, _win32_minidump_directory_str, base.minidump_directory_str, minidumpapiset/MINIDUMP_DIRECTORY, minidumpapiset/PMINIDUMP_DIRECTORY"
ms.prod: windows
ms.technology: windows-sdk
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
 - MINIDUMP_DIRECTORY
product: Windows
targetos: Windows
req.typenames: MINIDUMP_DIRECTORY, *PMINIDUMP_DIRECTORY
req.redist: DbgHelp.dll 5.1 or later
---

# _MINIDUMP_DIRECTORY structure


## -description


Contains the information needed to access a specific data stream in a minidump file.


## -struct-fields




### -field StreamType

The type of data stream. This member can be one of the values in the 
<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a> enumeration.


### -field Location

A 
<a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a> structure that specifies the location of the data stream.


## -remarks



In this context, a data stream is a block of data within a minidump file.




## -see-also




<a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>



<a href="https://msdn.microsoft.com/56df69aa-55b6-451b-a003-3ee88dc934f9">MiniDumpReadDumpStream</a>
 

 

