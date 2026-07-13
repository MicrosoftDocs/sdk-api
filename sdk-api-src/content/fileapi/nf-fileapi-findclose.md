---
UID: NF:fileapi.FindClose
title: FindClose function (fileapi.h)
description: Closes a file search handle opened by the FindFirstFile, FindFirstFileEx, FindFirstFileNameW, FindFirstFileNameTransactedW, FindFirstFileTransacted, FindFirstStreamTransactedW, or FindFirstStreamW functions.
helpviewer_keywords: ["FindClose","FindClose function [Files]","_win32_findclose","base.findclose","fileapi/FindClose","fs.findclose","winbase/FindClose"]
old-location: fs\findclose.htm
tech.root: fs
ms.assetid: 64b3bc49-1e0e-4572-9d9f-936c45f5b01c
ms.date: 12/05/2018
ms.keywords: FindClose, FindClose function [Files], _win32_findclose, base.findclose, fileapi/FindClose, fs.findclose, winbase/FindClose
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
 - FindClose
 - fileapi/FindClose
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
 - FindClose
---

# FindClose function


## -description

Closes a file search handle opened by the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a>, 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexa">FindFirstFileEx</a>, 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilenamew">FindFirstFileNameW</a>, 
    <a href="/windows/desktop/api/winbase/nf-winbase-findfirstfilenametransactedw">FindFirstFileNameTransactedW</a>, 
    <a href="/windows/desktop/api/winbase/nf-winbase-findfirstfiletransacteda">FindFirstFileTransacted</a>, 
    <a href="/windows/desktop/api/winbase/nf-winbase-findfirststreamtransactedw">FindFirstStreamTransactedW</a>, or 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw">FindFirstStreamW</a> functions.

## -parameters

### -param hFindFile [in, out]

The file search handle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After the <b>FindClose</b> function is called, the handle 
    specified by the <i>hFindFile</i> parameter cannot be used in subsequent calls to the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilea">FindNextFile</a>, 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew">FindNextFileNameW</a>, 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw">FindNextStreamW</a>, or 
    <b>FindClose</b> functions.

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
     <a href="/windows/desktop/FileIO/listing-the-files-in-a-directory">Listing the Files in a Directory</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexa">FindFirstFileEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findfirstfilenametransactedw">FindFirstFileNameTransactedW</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilenamew">FindFirstFileNameW</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findfirstfiletransacteda">FindFirstFileTransacted</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findfirststreamtransactedw">FindFirstStreamTransactedW</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw">FindFirstStreamW</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilea">FindNextFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew">FindNextFileNameW</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw">FindNextStreamW</a>