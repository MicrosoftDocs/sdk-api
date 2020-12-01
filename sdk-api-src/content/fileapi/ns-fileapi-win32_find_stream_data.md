---
UID: NS:fileapi._WIN32_FIND_STREAM_DATA
title: WIN32_FIND_STREAM_DATA (fileapi.h)
description: Contains information about the stream found by the FindFirstStreamW or FindNextStreamW function.
helpviewer_keywords: ["*PWIN32_FIND_STREAM_DATA","PWIN32_FIND_STREAM_DATA","PWIN32_FIND_STREAM_DATA structure pointer [Files]","WIN32_FIND_STREAM_DATA","WIN32_FIND_STREAM_DATA structure [Files]","_win32_win32_find_stream_data_str","base.win32_find_stream_data_str","fileapi/PWIN32_FIND_STREAM_DATA","fileapi/WIN32_FIND_STREAM_DATA","fs.win32_find_stream_data_str"]
old-location: fs\win32_find_stream_data_str.htm
tech.root: fs
ms.assetid: f21f5161-10a8-474c-85d8-dde075b9daff
ms.date: 12/05/2018
ms.keywords: '*PWIN32_FIND_STREAM_DATA, PWIN32_FIND_STREAM_DATA, PWIN32_FIND_STREAM_DATA structure pointer [Files], WIN32_FIND_STREAM_DATA, WIN32_FIND_STREAM_DATA structure [Files], _win32_win32_find_stream_data_str, base.win32_find_stream_data_str, fileapi/PWIN32_FIND_STREAM_DATA, fileapi/WIN32_FIND_STREAM_DATA, fs.win32_find_stream_data_str'
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
targetos: Windows
req.typenames: WIN32_FIND_STREAM_DATA, *PWIN32_FIND_STREAM_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WIN32_FIND_STREAM_DATA
 - fileapi/_WIN32_FIND_STREAM_DATA
 - PWIN32_FIND_STREAM_DATA
 - fileapi/PWIN32_FIND_STREAM_DATA
 - WIN32_FIND_STREAM_DATA
 - fileapi/WIN32_FIND_STREAM_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fileapi.h
api_name:
 - WIN32_FIND_STREAM_DATA
---

# WIN32_FIND_STREAM_DATA structure


## -description

Contains information about the stream found by the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw">FindFirstStreamW</a> or 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw">FindNextStreamW</a> function.

## -struct-fields

### -field StreamSize

A <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> value that specifies the 
      size of the stream, in bytes.

### -field cStreamName

The name of the stream. The string name format is 
      ":<i>streamname</i>:$<i>streamtype</i>".

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw">FindFirstStreamW</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw">FindNextStreamW</a>



<a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>