---
UID: NF:winbase.GetLongPathNameTransactedW
title: GetLongPathNameTransactedW function (winbase.h)
description: Converts the specified path to its long form as a transacted operation. (Unicode)
helpviewer_keywords: ["GetLongPathNameTransacted", "GetLongPathNameTransacted function [Files]", "GetLongPathNameTransactedW", "fs.getlongpathnametransacted", "winbase/GetLongPathNameTransacted", "winbase/GetLongPathNameTransactedW"]
old-location: fs\getlongpathnametransacted.htm
tech.root: fs
ms.assetid: 8523cde9-f0dd-4832-8d9d-9e68bac89344
ms.date: 12/05/2018
ms.keywords: GetLongPathNameTransacted, GetLongPathNameTransacted function [Files], GetLongPathNameTransactedA, GetLongPathNameTransactedW, fs.getlongpathnametransacted, winbase/GetLongPathNameTransacted, winbase/GetLongPathNameTransactedA, winbase/GetLongPathNameTransactedW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetLongPathNameTransactedW (Unicode) and GetLongPathNameTransactedA (ANSI)
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
 - GetLongPathNameTransactedW
 - winbase/GetLongPathNameTransactedW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetLongPathNameTransacted
 - GetLongPathNameTransactedA
 - GetLongPathNameTransactedW
---

# GetLongPathNameTransactedW function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Converts the specified path to its long form as a transacted operation.

To perform this operation without a transaction, use the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getlongpathnamea">GetLongPathName</a> function.

For more information about file and path names, see 
    <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>.

## -parameters

### -param lpszShortPath [in]

The path to be converted.

The path must reside on the local computer; otherwise, the function fails and the last error code is set to 
      <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpszLongPath [out]

A pointer to the buffer to receive the long path.

You can use the same buffer you used for the <i>lpszShortPath</i> parameter.

### -param cchBuffer [in]

The size of the buffer <i>lpszLongPath</i> points to, in 
      <b>TCHAR</b>s.

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is the length, in <b>TCHAR</b>s, of the 
       string copied to <i>lpszLongPath</i>, not including the terminating null character.

If the <i>lpBuffer</i> buffer is too small to contain the path, the return value is the 
       size, in <b>TCHAR</b>s, of the buffer that is required to hold the path and the 
       terminating null character.

If the function fails for any other reason, such as if the file does not exist, the return value is zero. To 
       get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

On many file systems, a short file name contains a tilde (~) character. However, not all file systems follow 
    this convention. Therefore, do not assume that you can skip calling 
    <b>GetLongPathNameTransacted</b> if the path does not 
    contain a tilde (~) character.

If a long path is not found, this function returns the name specified in the 
    <i>lpszShortPath</i> parameter in the <i>lpszLongPath</i> parameter.

If the return value is greater than the value specified in <i>cchBuffer</i>, you can call 
    the function again with a buffer that is large enough to hold the path. For an example of this case, see the 
    Example Code section for <a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a>.

<div class="alert"><b>Note</b>  Although the return value in this case is a length that includes the terminating null character, the return 
     value on success does not include the terminating null character in the count.</div>
<div> </div>
It is possible to have access to a file or directory but not have access to some of the parent directories of 
    that file or directory. As a result, 
    <b>GetLongPathNameTransacted</b> may fail when it is 
    unable to query the parent directory of a path component to determine the long name for that component. This check 
    can be skipped for directory components that have file extensions longer than 3 characters, or total lengths 
    longer than 12 characters. For more information, see the 
    <a href="/windows/desktop/FileIO/naming-a-file">Short vs. Long Names</a> section of 
    <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>.

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





> [!NOTE]
> The winbase.h header defines GetLongPathNameTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfullpathnametransacteda">GetFullPathNameTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getshortpathnamew">GetShortPathName</a>



<a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
