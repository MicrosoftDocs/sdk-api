---
UID: NF:winbase.FindFirstStreamTransactedW
title: FindFirstStreamTransactedW function (winbase.h)
description: Enumerates the first stream in the specified file or directory as a transacted operation.
helpviewer_keywords: ["FindFirstStreamTransactedW","FindFirstStreamTransactedW function [Files]","FindStreamInfoStandard","fs.findfirststreamtransactedw","winbase/FindFirstStreamTransactedW"]
old-location: fs\findfirststreamtransactedw.htm
tech.root: fs
ms.assetid: 76c64aa9-0501-457d-b774-c209fbac4ccc
ms.date: 12/05/2018
ms.keywords: FindFirstStreamTransactedW, FindFirstStreamTransactedW function [Files], FindStreamInfoStandard, fs.findfirststreamtransactedw, winbase/FindFirstStreamTransactedW
req.header: winbase.h
req.include-header: Windows.h
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
 - FindFirstStreamTransactedW
 - winbase/FindFirstStreamTransactedW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - FindFirstStreamTransactedW
---

# FindFirstStreamTransactedW function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Enumerates the first stream in the specified file or directory as a transacted 
    operation.

## -parameters

### -param lpFileName [in]

The fully qualified file name.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to 
       <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b> (6805).

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

A pointer to a buffer that receives the file data. The format of this data depends on the value of 
       the <i>InfoLevel</i> parameter.

### -param dwFlags

Reserved for future use. This parameter must be zero.

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
       <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is a search handle that can be used in subsequent calls to the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw">FindNextStreamW</a> function.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All files contain a default data stream. On NTFS, files can also contain one or more named data streams. On 
    FAT file systems, files cannot have more that the default data stream, and therefore, this function will not 
    return valid results when used on FAT filesystem files. This function works on all file systems that supports hard 
    links; otherwise, the function returns <b>ERROR_STATUS_NOT_IMPLEMENTED</b> (6805).

The <b>FindFirstStreamTransactedW</b> function 
    opens a search handle and returns information about the first stream in the specified file or directory. For 
    files, this is always the default data stream, ::$DATA. After the search handle has been established, use it in 
    the <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw">FindNextStreamW</a> function to search for other 
    streams in the specified file or directory. When the search handle is no longer needed, it should be closed using 
    the <a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a> function.

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
No

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
No

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
No

</td>
</tr>
</table>
 

SMB 3.0 does not support TxF.

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw">FindNextStreamW</a>



<a href="/windows/desktop/api/fileapi/ne-fileapi-stream_info_levels">STREAM_INFO_LEVELS</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>



<a href="/windows/desktop/api/fileapi/ns-fileapi-win32_find_stream_data">WIN32_FIND_STREAM_DATA</a>