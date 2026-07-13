---
UID: NF:fileapi.FindFirstStreamW
title: FindFirstStreamW function (fileapi.h)
description: Enumerates the first stream with a ::$DATA stream type in the specified file or directory.
helpviewer_keywords: ["FindFirstStreamW","FindFirstStreamW function [Files]","FindStreamInfoStandard","_win32_findfirststreamw","base.findfirststreamw","fileapi/FindFirstStreamW","fs.findfirststreamw"]
old-location: fs\findfirststreamw.htm
tech.root: fs
ms.assetid: aab3af94-a2e0-45ad-a846-f457408a19d5
ms.date: 12/05/2018
ms.keywords: FindFirstStreamW, FindFirstStreamW function [Files], FindStreamInfoStandard, _win32_findfirststreamw, base.findfirststreamw, fileapi/FindFirstStreamW, fs.findfirststreamw
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
 - FindFirstStreamW
 - fileapi/FindFirstStreamW
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
 - FindFirstStreamW
---

# FindFirstStreamW function


## -description

Enumerates the first stream with a ::$DATA stream type in the specified file or 
    directory.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-findfirststreamtransactedw">FindFirstStreamTransactedW</a> 
    function.

## -parameters

### -param lpFileName [in]

The fully qualified file name.

### -param InfoLevel [in]

The information level of the returned data. This parameter is one of the values in the 
      <a href="/windows/desktop/api/fileapi/ne-fileapi-stream_info_levels">STREAM_INFO_LEVELS</a> enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FindStreamInfoStandard"></a><a id="findstreaminfostandard"></a><a id="FINDSTREAMINFOSTANDARD"></a><dl>
<dt><b>FindStreamInfoStandard</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The data is returned in a 
        <a href="/windows/desktop/api/fileapi/ns-fileapi-win32_find_stream_data">WIN32_FIND_STREAM_DATA</a> structure.

</td>
</tr>
</table>

### -param lpFindStreamData [out]

A pointer to a buffer that receives the file stream data. The format of this data depends on the value of 
      the <i>InfoLevel</i> parameter.

### -param dwFlags

Reserved for future use. This parameter must be zero.

## -returns

If the function succeeds, the return value is a search handle that can be used in subsequent calls to the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw">FindNextStreamW</a> function.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If no  streams can be found, the function fails and 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
       <b>ERROR_HANDLE_EOF</b> (38).
       
If the filesystem does not support streams, the function fails and
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
       <b>ERROR_INVALID_PARAMETER</b> (87).


## -remarks

The <b>FindFirstStreamW</b> function opens a search handle and returns information about the first
    $DATA stream in the specified file or directory.
    For files, this is always the default, unnamed data stream, "::$DATA". Directories do not have $DATA streams by default
    and cannot have an unnamed data stream, but may have named data streams set after they have been created.
    After the search handle has been established, use it in calls to the
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw">FindNextStreamW</a> function to 
    search for other streams in the specified file or directory. When the search handle is no longer needed, it should 
    be closed using the <a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a> function.

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
 

SMB 3.0 supports list of streams less than or equal to 64K.

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findfirststreamtransactedw">FindFirstStreamTransactedW</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw">FindNextStreamW</a>



<a href="/windows/desktop/api/fileapi/ne-fileapi-stream_info_levels">STREAM_INFO_LEVELS</a>



<a href="/windows/desktop/api/fileapi/ns-fileapi-win32_find_stream_data">WIN32_FIND_STREAM_DATA</a>