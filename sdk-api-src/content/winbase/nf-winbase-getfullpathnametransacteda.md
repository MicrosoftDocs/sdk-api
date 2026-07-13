---
UID: NF:winbase.GetFullPathNameTransactedA
title: GetFullPathNameTransactedA function (winbase.h)
description: Retrieves the full path and file name of the specified file as a transacted operation. (ANSI)
helpviewer_keywords: ["GetFullPathNameTransactedA", "winbase/GetFullPathNameTransactedA"]
old-location: fs\getfullpathnametransacted.htm
tech.root: fs
ms.assetid: 63cbcec6-e9f0-4db3-bf2f-03a987000af1
ms.date: 12/05/2018
ms.keywords: GetFullPathNameTransacted, GetFullPathNameTransacted function [Files], GetFullPathNameTransactedA, GetFullPathNameTransactedW, fs.getfullpathnametransacted, winbase/GetFullPathNameTransacted, winbase/GetFullPathNameTransactedA, winbase/GetFullPathNameTransactedW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFullPathNameTransactedW (Unicode) and GetFullPathNameTransactedA (ANSI)
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
 - GetFullPathNameTransactedA
 - winbase/GetFullPathNameTransactedA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetFullPathNameTransacted
 - GetFullPathNameTransactedA
 - GetFullPathNameTransactedW
---

# GetFullPathNameTransactedA function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Retrieves the full path and file name of the specified file as a transacted operation.

To perform this operation without transactions, use the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a> function.

For more information about file and path names, see 
    <a href="/windows/desktop/FileIO/naming-a-file">File Names, Paths, and Namespaces</a>.

## -parameters

### -param lpFileName [in]

The name of the file.

This string can use short (the 8.3 form) or long file names. This string can be a share or volume name.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to 
       <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

### -param nBufferLength [in]

The size of the buffer to receive the null-terminated string  for the drive and path,  in 
      <b>TCHARs</b>.

### -param lpBuffer [out]

A pointer to a buffer that receives the null-terminated string for the  drive and path.

### -param lpFilePart [out]

A pointer to a buffer that receives the address (in <i>lpBuffer</i>) of the final file 
       name component in the path. Specify <b>NULL</b> if you do not need to receive this 
       information.

If <i>lpBuffer</i> points to a directory and not a file, 
       <i>lpFilePart</i> receives 0 (zero).

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the 
       string copied to <i>lpBuffer</i>, not including the terminating null character.

If the <i>lpBuffer</i> buffer is too small to contain the path, the return value is the 
       size, in <b>TCHARs</b>, of the buffer that is required to hold the path and the 
       terminating null character.

If the function fails for any other reason, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>GetFullPathNameTransacted</b> merges the name 
    of the current drive and directory with a specified file name to determine the full path and file name of a 
    specified file. It also calculates the address of the file name portion of the full path and file name. This 
    function does not verify that the resulting path and file name are valid, or that they see an existing file on the 
    associated volume.

Share and volume names are valid input for <i>lpFileName</i>. For example, the following 
    list identities the returned path and file names if test-2 is a remote computer and U: is a network mapped drive:

<ul>
<li>If you specify "\\test-2\q$\lh" the path returned is 
      "\\test-2\q$\lh"</li>
<li>If you specify "\\?\UNC\test-2\q$\lh" the path returned is 
      "\\?\UNC\test-2\q$\lh"</li>
<li>If you specify "U:" the path returned is "U:\"</li>
</ul>
<b>GetFullPathNameTransacted</b> does not convert 
    the specified file name, <i>lpFileName</i>. If the specified file name exists, you can use 
    <a href="/windows/desktop/api/winbase/nf-winbase-getlongpathnametransacteda">GetLongPathNameTransacted</a>, 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getlongpathnamea">GetLongPathName</a>, or 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getshortpathnamew">GetShortPathName</a> to convert to long or short path 
    names, respectively.

If the return value is greater than the value specified in <i>nBufferLength</i>, you can 
    call the function again with a buffer that is large enough to hold the path. For an example of this case as well 
    as using zero length buffer for dynamic allocation, see the Example Code section.

<div class="alert"><b>Note</b>  Although the return value in this case is a length that includes the terminating null character, the return 
     value on success does not include the terminating null character in the count.</div>
<div> </div>
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
> The winbase.h header defines GetFullPathNameTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getlongpathnametransacteda">GetLongPathNameTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getshortpathnamew">GetShortPathName</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-gettemppatha">GetTempPath</a>



<a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
