---
UID: NS:fileapi._WIN32_FIND_STREAM_DATA
title: "_WIN32_FIND_STREAM_DATA"
author: windows-sdk-content
description: Contains information about the stream found by the FindFirstStreamW or FindNextStreamW function.
old-location: fs\win32_find_stream_data_str.htm
tech.root: fileio
ms.assetid: f21f5161-10a8-474c-85d8-dde075b9daff
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PWIN32_FIND_STREAM_DATA, PWIN32_FIND_STREAM_DATA, PWIN32_FIND_STREAM_DATA structure pointer [Files], WIN32_FIND_STREAM_DATA, WIN32_FIND_STREAM_DATA structure [Files], _WIN32_FIND_STREAM_DATA, _win32_win32_find_stream_data_str, base.win32_find_stream_data_str, fileapi/PWIN32_FIND_STREAM_DATA, fileapi/WIN32_FIND_STREAM_DATA, fs.win32_find_stream_data_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - fileapi.h
api_name:
 - WIN32_FIND_STREAM_DATA
product: Windows
targetos: Windows
req.typenames: WIN32_FIND_STREAM_DATA, *PWIN32_FIND_STREAM_DATA
req.redist: 
---

# _WIN32_FIND_STREAM_DATA structure


## -description


Contains information about the stream found by the 
    <a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a> or 
    <a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a> function.


## -struct-fields




### -field StreamSize

A <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> value that specifies the 
      size of the stream, in bytes.


### -field cStreamName

The name of the stream. The string name format is 
      ":<i>streamname</i>:$<i>streamtype</i>".


## -see-also




<a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a>



<a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>
 

 

