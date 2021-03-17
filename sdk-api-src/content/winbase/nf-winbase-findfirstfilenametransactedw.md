---
UID: NF:winbase.FindFirstFileNameTransactedW
title: FindFirstFileNameTransactedW function (winbase.h)
description: Creates an enumeration of all the hard links to the specified file as a transacted operation. The function returns a handle to the enumeration that can be used on subsequent calls to the FindNextFileNameW function.
helpviewer_keywords: ["FindFirstFileNameTransactedW","FindFirstFileNameTransactedW function [Files]","fs.findfirstfilenametransactedw","winbase/FindFirstFileNameTransactedW"]
old-location: fs\findfirstfilenametransactedw.htm
tech.root: fs
ms.assetid: 79c7d32d-3cb7-4e27-9db1-f24282bf606a
ms.date: 12/05/2018
ms.keywords: FindFirstFileNameTransactedW, FindFirstFileNameTransactedW function [Files], fs.findfirstfilenametransactedw, winbase/FindFirstFileNameTransactedW
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
 - FindFirstFileNameTransactedW
 - winbase/FindFirstFileNameTransactedW
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
 - FindFirstFileNameTransactedW
---

# FindFirstFileNameTransactedW function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Creates an enumeration of all the hard links to the specified file as a transacted operation. The 
    function returns a handle to the enumeration that can be used on subsequent calls to the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew">FindNextFileNameW</a> function.

## -parameters

### -param lpFileName [in]

The name of the file.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to 
       <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b> (6805).

### -param dwFlags [in]

Reserved; specify zero (0).

### -param StringLength [in, out]

The size of the buffer pointed to by the <i>LinkName</i> parameter, in characters. If this 
       call fails and the error is <b>ERROR_MORE_DATA</b> (234), the value that is returned by this 
       parameter is the size that the buffer pointed to by <i>LinkName</i> must be to contain all 
       the data.

### -param LinkName [in, out]

A pointer to a buffer to store the first link name found for <i>lpFileName</i>.

### -param hTransaction [in, optional]

A handle to the transaction. This handle is returned by the 
       <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is a search handle that can be used with the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew">FindNextFileNameW</a> function or closed with the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a> function.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b> (0xffffffff). To  
      get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> 
      function.

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



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew">FindNextFileNameW</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>