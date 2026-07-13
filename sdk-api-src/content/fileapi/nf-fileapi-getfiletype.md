---
UID: NF:fileapi.GetFileType
title: GetFileType function (fileapi.h)
description: Retrieves the file type of the specified file.
helpviewer_keywords: ["GetFileType","GetFileType function [Files]","_win32_getfiletype","base.getfiletype","fileapi/GetFileType","fs.getfiletype","winbase/GetFileType"]
old-location: fs\getfiletype.htm
tech.root: fs
ms.assetid: 11760e2f-5e8b-4ec7-959b-fb23d5d9a0aa
ms.date: 12/05/2018
ms.keywords: GetFileType, GetFileType function [Files], _win32_getfiletype, base.getfiletype, fileapi/GetFileType, fs.getfiletype, winbase/GetFileType
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - GetFileType
 - fileapi/GetFileType
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
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetFileType
---

# GetFileType function


## -description

Retrieves the file type of the specified file.

## -parameters

### -param hFile [in]

A handle to the file.

## -returns

The function returns one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILE_TYPE_CHAR</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The specified file is a character file, typically an LPT device or a console.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILE_TYPE_DISK</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The specified file is a disk file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILE_TYPE_PIPE</b></dt>
<dt>0x0003</dt>
</dl>
</td>
<td width="60%">
The specified file is a socket, a named pipe, or an anonymous pipe.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILE_TYPE_REMOTE</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
Unused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILE_TYPE_UNKNOWN</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Either the type of the specified file is unknown, or the function failed.

</td>
</tr>
</table>
 

You can distinguish between a "valid" return of <b>FILE_TYPE_UNKNOWN</b> and its return due to a calling error (for example, passing an invalid handle to 
<b>GetFileType</b>) by calling 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the function worked properly and <b>FILE_TYPE_UNKNOWN</b> was returned, a call to <b>GetLastError</b> will return <b>NO_ERROR</b>.

If the function returned <b>FILE_TYPE_UNKNOWN</b> due to an error in calling 
<b>GetFileType</b>, 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return the error code.

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



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfilesize">GetFileSize</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfiletime">GetFileTime</a>