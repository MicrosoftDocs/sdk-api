---
UID: NF:fileapi.FlushFileBuffers
title: FlushFileBuffers function (fileapi.h)
description: Flushes the buffers of a specified file and causes all buffered data to be written to a file.
old-location: fs\flushfilebuffers.htm
tech.root: FileIO
ms.assetid: 0d9ea467-6d5d-44b2-8e87-f2ecdd510fe6
ms.date: 12/05/2018
ms.keywords: FlushFileBuffers, FlushFileBuffers function [Files], _win32_flushfilebuffers, base.flushfilebuffers, fileapi/FlushFileBuffers, fs.flushfilebuffers, winbase/FlushFileBuffers
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
 - FlushFileBuffers
 - fileapi/FlushFileBuffers
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
 - FlushFileBuffers
---

# FlushFileBuffers function


## -description

Flushes the buffers of a specified file and causes all buffered data to be written to a file.

## -parameters

### -param hFile [in]

A handle to the open file. 

The file handle must have the <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

If <i>hFile</i> is a handle to a communications device, the function only flushes the transmit buffer.

If <i>hFile</i> is a handle to the server end of a named pipe, the function does not return until the client has read all buffered data from the pipe.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The function fails if <i>hFile</i> is a handle to the console output. That is because the console output is not buffered. The function returns <b>FALSE</b>, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INVALID_HANDLE</b>.

## -remarks

Typically the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> and 
<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a> functions write data to an internal buffer that the operating system writes to a disk or communication pipe on a regular basis. The 
<b>FlushFileBuffers</b> function writes all the buffered information for a specified file to the device or pipe.

Due to disk caching interactions within the system, the 
<b>FlushFileBuffers</b> function can be inefficient when used after every write to a disk drive device when many writes are being performed separately. If an application is  performing multiple writes to disk and also needs to ensure critical data is 
written to persistent media, the application should use unbuffered I/O  instead of frequently calling <b>FlushFileBuffers</b>. To open a file for unbuffered I/O, call the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function with the <b>FILE_FLAG_NO_BUFFERING</b> and <b>FILE_FLAG_WRITE_THROUGH</b> flags. This prevents the file contents from being cached and flushes the metadata to disk with each write. For more information, see <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

To flush all open files on a volume, call <b>FlushFileBuffers</b> with a handle to the volume. The caller must have administrative privileges. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>. 

When opening a volume with <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>, the <i>lpFileName</i> string should be the following form: &#92;&#92;.&#92;<i>x</i>: or &#92;&#92;?&#92;Volume{<i>GUID</i>}. Do not use a trailing backslash in the volume name, because that indicates the root directory of a drive.  

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
<a href="/windows/desktop/ipc/multithreaded-pipe-server">Multithreaded Pipe Server</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>
