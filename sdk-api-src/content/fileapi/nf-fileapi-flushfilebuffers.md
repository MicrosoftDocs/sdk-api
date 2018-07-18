---
UID: NF:fileapi.FlushFileBuffers
title: FlushFileBuffers function
author: windows-sdk-content
description: Flushes the buffers of a specified file and causes all buffered data to be written to a file.
old-location: fs\flushfilebuffers.htm
old-project: fileio
ms.assetid: 0d9ea467-6d5d-44b2-8e87-f2ecdd510fe6
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: FlushFileBuffers, FlushFileBuffers function [Files], _win32_flushfilebuffers, base.flushfilebuffers, fileapi/FlushFileBuffers, fs.flushfilebuffers, winbase/FlushFileBuffers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - FlushFileBuffers
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# FlushFileBuffers function


## -description


Flushes the buffers of a specified file and causes all buffered data to be written to a file.


## -parameters




### -param hFile [in]

A handle to the open file. 

The file handle must have the <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.

If <i>hFile</i> is a handle to a communications device, the function only flushes the transmit buffer.

If <i>hFile</i> is a handle to the server end of a named pipe, the function does not return until the client has read all buffered data from the pipe.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The function fails if <i>hFile</i> is a handle to the console output. That is because the console output is not buffered. The function returns <b>FALSE</b>, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INVALID_HANDLE</b>.




## -remarks



Typically the 
<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> and 
<a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a> functions write data to an internal buffer that the operating system writes to a disk or communication pipe on a regular basis. The 
<b>FlushFileBuffers</b> function writes all the buffered information for a specified file to the device or pipe.

Due to disk caching interactions within the system, the 
<b>FlushFileBuffers</b> function can be inefficient when used after every write to a disk drive device when many writes are being performed separately. If an application is  performing multiple writes to disk and also needs to ensure critical data is 
written to persistent media, the application should use unbuffered I/O  instead of frequently calling <b>FlushFileBuffers</b>. To open a file for unbuffered I/O, call the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function with the <b>FILE_FLAG_NO_BUFFERING</b> and <b>FILE_FLAG_WRITE_THROUGH</b> flags. This prevents the file contents from being cached and flushes the metadata to disk with each write. For more information, see <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.

To flush all open files on a volume, call <b>FlushFileBuffers</b> with a handle to the volume. The caller must have administrative privileges. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>. 

When opening a volume with <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>, the <i>lpFileName</i> string should be the following form: \\.\<i>x</i>: or \\?\Volume{<i>GUID</i>}. Do not use a trailing backslash in the volume name, because that indicates the root directory of a drive.  

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
 


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/4657e814-0e7f-45b5-8ddb-17ec0c3612ba">Multithreaded Pipe Server</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>



<a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a>
 

 

