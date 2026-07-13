---
UID: NF:fileapi.FindNextFileNameW
title: FindNextFileNameW function (fileapi.h)
description: Continues enumerating the hard links to a file using the handle returned by a successful call to the FindFirstFileNameW function.
helpviewer_keywords: ["FindNextFileNameW","FindNextFileNameW function [Files]","fileapi/FindNextFileNameW","fs.findnextfilenamew"]
old-location: fs\findnextfilenamew.htm
tech.root: fs
ms.assetid: 1d2f8041-2744-4f37-afde-ddce49a8bdc5
ms.date: 12/05/2018
ms.keywords: FindNextFileNameW, FindNextFileNameW function [Files], fileapi/FindNextFileNameW, fs.findnextfilenamew
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FindNextFileNameW
 - fileapi/FindNextFileNameW
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
 - api-ms-win-core-file-l1-2-1.dll
 - api-ms-win-core-file-l1-2-0.dll
 - api-ms-win-core-file-l1-1-0.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-L1-2-2.dll
 - KernelBase.dll
api_name:
 - FindNextFileNameW
---

# FindNextFileNameW function


## -description

Continues enumerating the hard links to a file using the handle returned by a successful call to the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilenamew">FindFirstFileNameW</a> function.

## -parameters

### -param hFindStream [in]

A handle to the enumeration that is returned by a successful call to 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilenamew">FindFirstFileNameW</a>.

### -param StringLength [in, out]

The size of the <i>LinkName</i> parameter, in characters. If this call fails and the 
      error is <b>ERROR_MORE_DATA</b>, the value that is returned by this parameter is the size 
      that <i>LinkName</i>  must be to contain all the data.

### -param LinkName [in, out]

A pointer to a buffer to store the first link name found for <i>lpFileName</i>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If no matching files can be found, the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> 
       function returns <b>ERROR_HANDLE_EOF</b>.

## -remarks

If the function returns <b>TRUE</b>, there are more hard links to enumerate.

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
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

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



<a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilenamew">FindFirstFileNameW</a>