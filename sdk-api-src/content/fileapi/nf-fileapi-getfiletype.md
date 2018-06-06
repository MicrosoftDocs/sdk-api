---
UID: NF:fileapi.GetFileType
title: GetFileType function
author: windows-sdk-content
description: Retrieves the file type of the specified file.
old-location: fs\getfiletype.htm
old-project: FileIO
ms.assetid: 11760e2f-5e8b-4ec7-959b-fb23d5d9a0aa
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetFileType, GetFileType function [Files], _win32_getfiletype, base.getfiletype, fileapi/GetFileType, fs.getfiletype, winbase/GetFileType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: STREAM_INFO_LEVELS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the function worked properly and <b>FILE_TYPE_UNKNOWN</b> was returned, a call to <b>GetLastError</b> will return <b>NO_ERROR</b>.

If the function returned <b>FILE_TYPE_UNKNOWN</b> due to an error in calling 
<b>GetFileType</b>, 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return the error code.
                  




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




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/3f5d2e4a-1e05-41c0-9b7e-0155e212f6dd">GetFileSize</a>



<a href="https://msdn.microsoft.com/7f88e1c8-4328-40c2-857d-745e4a1d350d">GetFileTime</a>
 

 

