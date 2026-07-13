---
UID: NF:fileapi.FindNextStreamW
title: FindNextStreamW function (fileapi.h)
description: Continues a stream search started by a previous call to the FindFirstStreamW function.
helpviewer_keywords: ["FindNextStreamW","FindNextStreamW function [Files]","_win32_findnextstreamw","base.findnextstreamw","fileapi/FindNextStreamW","fs.findnextstreamw"]
old-location: fs\findnextstreamw.htm
tech.root: fs
ms.assetid: 2bb0301c-b2be-4056-913c-e4102386135e
ms.date: 12/05/2018
ms.keywords: FindNextStreamW, FindNextStreamW function [Files], _win32_findnextstreamw, base.findnextstreamw, fileapi/FindNextStreamW, fs.findnextstreamw
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FindNextStreamW
 - fileapi/FindNextStreamW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - FindNextStreamW
---

# FindNextStreamW function


## -description

Continues a stream search started by a previous call to the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw">FindFirstStreamW</a> function.

## -parameters

### -param hFindStream [in]

The search handle returned by a previous call to the 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw">FindFirstStreamW</a> function.

### -param lpFindStreamData [out]

A pointer to the 
      <a href="/windows/desktop/api/fileapi/ns-fileapi-win32_find_stream_data">WIN32_FIND_STREAM_DATA</a> structure that 
      receives information about the stream.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If no  more streams can be found, 
       <b>GetLastError</b> returns 
       <b>ERROR_HANDLE_EOF</b> (38).

## -remarks

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw">FindFirstStreamW</a>



<a href="/windows/desktop/api/fileapi/ns-fileapi-win32_find_stream_data">WIN32_FIND_STREAM_DATA</a>