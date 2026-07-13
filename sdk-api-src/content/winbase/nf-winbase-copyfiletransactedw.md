---
UID: NF:winbase.CopyFileTransactedW
title: CopyFileTransactedW function (winbase.h)
description: Copies an existing file to a new file as a transacted operation, notifying the application of its progress through a callback function. (Unicode)
helpviewer_keywords: ["COPY_FILE_COPY_SYMLINK", "COPY_FILE_FAIL_IF_EXISTS", "COPY_FILE_OPEN_SOURCE_FOR_WRITE", "COPY_FILE_RESTARTABLE", "CopyFileTransacted", "CopyFileTransacted function [Files]", "CopyFileTransactedW", "fs.copyfiletransacted", "winbase/CopyFileTransacted", "winbase/CopyFileTransactedW"]
old-location: fs\copyfiletransacted.htm
tech.root: fs
ms.assetid: 118392de-166b-413e-99c9-b3deb756de0e
ms.date: 12/05/2018
ms.keywords: COPY_FILE_COPY_SYMLINK, COPY_FILE_FAIL_IF_EXISTS, COPY_FILE_OPEN_SOURCE_FOR_WRITE, COPY_FILE_RESTARTABLE, CopyFileTransacted, CopyFileTransacted function [Files], CopyFileTransactedA, CopyFileTransactedW, fs.copyfiletransacted, winbase/CopyFileTransacted, winbase/CopyFileTransactedA, winbase/CopyFileTransactedW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CopyFileTransactedW (Unicode) and CopyFileTransactedA (ANSI)
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
 - CopyFileTransactedW
 - winbase/CopyFileTransactedW
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
 - CopyFileTransacted
 - CopyFileTransactedA
 - CopyFileTransactedW
---

# CopyFileTransactedW function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Copies an existing file to a new file as a transacted operation, notifying the application of its 
    progress through a callback function.

## -parameters

### -param lpExistingFileName [in]

The name of an existing file.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

If <i>lpExistingFileName</i> does not exist, the 
       <b>CopyFileTransacted</b> function fails, and the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns 
       <b>ERROR_FILE_NOT_FOUND</b>.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to 
       <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

### -param lpNewFileName [in]

The name of the new file.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpProgressRoutine [in, optional]

The address of a callback function of type <b>LPPROGRESS_ROUTINE</b> that is called 
      each time another portion of the file has been copied. This parameter can be <b>NULL</b>. For 
      more information on the progress callback function, see the 
      <a href="/windows/desktop/api/winbase/nc-winbase-lpprogress_routine">CopyProgressRoutine</a> function.

### -param lpData [in, optional]

The argument to be passed to the callback function. This parameter can be 
      <b>NULL</b>.

### -param pbCancel [in, optional]

If this flag is set to <b>TRUE</b> during the copy operation, the operation is canceled. 
      Otherwise, the copy operation will continue to completion.

### -param dwCopyFlags [in]

Flags that specify how the file is to be copied. This parameter can be a combination of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_COPY_SYMLINK"></a><a id="copy_file_copy_symlink"></a><dl>
<dt><b>COPY_FILE_COPY_SYMLINK</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
If the source file is a symbolic link, the destination file is also a symbolic link pointing to the same 
        file that the source symbolic link is pointing to.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_FAIL_IF_EXISTS"></a><a id="copy_file_fail_if_exists"></a><dl>
<dt><b>COPY_FILE_FAIL_IF_EXISTS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The copy operation fails immediately if the target file already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_OPEN_SOURCE_FOR_WRITE"></a><a id="copy_file_open_source_for_write"></a><dl>
<dt><b>COPY_FILE_OPEN_SOURCE_FOR_WRITE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The file is copied and the original file is opened for write access.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_RESTARTABLE"></a><a id="copy_file_restartable"></a><dl>
<dt><b>COPY_FILE_RESTARTABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Progress of the copy is tracked in the target file in case the copy fails. The failed copy can be 
        restarted at a later time by specifying the same values for <i>lpExistingFileName</i> and 
        <i>lpNewFileName</i> as those used in the call that failed. This can significantly slow 
        down the copy operation as the new file may be flushed multiple times during the copy operation.

</td>
</tr>
</table>

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If <i>lpProgressRoutine</i> returns <b>PROGRESS_CANCEL</b> due to the 
       user canceling the operation, <b>CopyFileTransacted</b> 
       will return zero and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
       <b>ERROR_REQUEST_ABORTED</b>. In this case, the partially copied destination file is 
       deleted.

If <i>lpProgressRoutine</i> returns <b>PROGRESS_STOP</b> due to the 
       user stopping the operation, <b>CopyFileTransacted</b> 
       will return zero and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
       <b>ERROR_REQUEST_ABORTED</b>. In this case, the partially copied destination file is left 
       intact.

If you attempt to call this function with a handle to a transaction that has already been rolled back, 
       <b>CopyFileTransacted</b> will return either 
       <b>ERROR_TRANSACTION_NOT_ACTIVE</b> or 
       <b>ERROR_INVALID_TRANSACTION</b>.

## -remarks

This function preserves extended attributes, OLE structured storage, NTFS file system alternate data streams, 
     security attributes, and file attributes.

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008 and Windows Vista:  </b>Security resource attributes (<b>ATTRIBUTE_SECURITY_INFORMATION</b>) for the existing 
      file are not copied to the new file until Windows 8 and Windows Server 2012.

This function fails with <b>ERROR_ACCESS_DENIED</b> if the destination file already exists 
    and has the  <b>FILE_ATTRIBUTE_HIDDEN</b> or <b>FILE_ATTRIBUTE_READONLY</b> 
    attribute set.

Encrypted files are not supported by TxF.


If <b>COPY_FILE_COPY_SYMLINK</b> is specified, the following rules apply:

<ul>
<li>If the source file is a symbolic link, the symbolic link is copied, not the target file.</li>
<li>If  the source file is not a symbolic link, there is no change in behavior.</li>
<li>If the destination file is an existing symbolic link, the symbolic link is overwritten, not the target 
       file.</li>
<li>If <b>COPY_FILE_FAIL_IF_EXISTS</b> is also specified, and the destination file is an 
       existing symbolic link, the operation fails in all cases.</li>
</ul>
If <b>COPY_FILE_COPY_SYMLINK</b> is not specified, the following rules apply:

<ul>
<li>If <b>COPY_FILE_FAIL_IF_EXISTS</b> is also specified, and the destination file is an 
       existing symbolic link, the operation fails only if the target of the symbolic link exists.</li>
<li>If <b>COPY_FILE_FAIL_IF_EXISTS</b> is not specified, there is no change in 
       behavior.</li>
</ul>


Link tracking is not supported by TxF.

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
 

Note that SMB 3.0 does not support TxF.





> [!NOTE]
> The winbase.h header defines CopyFileTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nc-winbase-lpprogress_routine">CopyProgressRoutine</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a>



<a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefiletransacteda">MoveFileTransacted</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
