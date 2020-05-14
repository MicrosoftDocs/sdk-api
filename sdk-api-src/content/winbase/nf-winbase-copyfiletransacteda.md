---
UID: NF:winbase.CopyFileTransactedA
title: CopyFileTransactedA function (winbase.h)
description: Copies an existing file to a new file as a transacted operation, notifying the application of its progress through a callback function.helpviewer_keywords: ["COPY_FILE_COPY_SYMLINK","COPY_FILE_FAIL_IF_EXISTS","COPY_FILE_OPEN_SOURCE_FOR_WRITE","COPY_FILE_RESTARTABLE","CopyFileTransacted","CopyFileTransacted function [Files]","CopyFileTransactedA","CopyFileTransactedW","fs.copyfiletransacted","winbase/CopyFileTransacted","winbase/CopyFileTransactedA","winbase/CopyFileTransactedW"]
old-location: fs\copyfiletransacted.htm
tech.root: FileIO
ms.assetid: 118392de-166b-413e-99c9-b3deb756de0e
ms.date: 12/05/2018
ms.keywords: COPY_FILE_COPY_SYMLINK, COPY_FILE_FAIL_IF_EXISTS, COPY_FILE_OPEN_SOURCE_FOR_WRITE, COPY_FILE_RESTARTABLE, CopyFileTransacted, CopyFileTransacted function [Files], CopyFileTransactedA, CopyFileTransactedW, fs.copyfiletransacted, winbase/CopyFileTransacted, winbase/CopyFileTransactedA, winbase/CopyFileTransactedW
f1_keywords:
- winbase/CopyFileTransacted
dev_langs:
- c++
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
- CopyFileTransacted
- CopyFileTransactedA
- CopyFileTransactedW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CopyFileTransactedA function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Copies an existing file to a new file as a transacted operation, notifying the application of its 
    progress through a callback function.


## -parameters




### -param lpExistingFileName [in]

The name of an existing file.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">Naming a File</a>.

If <i>lpExistingFileName</i> does not exist, the 
       <b>CopyFileTransacted</b> function fails, and the 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns 
       <b>ERROR_FILE_NOT_FOUND</b>.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to 
       <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.


### -param lpNewFileName [in]

The name of the new file.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">Naming a File</a>.


### -param lpProgressRoutine [in, optional]

The address of a callback function of type <b>LPPROGRESS_ROUTINE</b> that is called 
      each time another portion of the file has been copied. This parameter can be <b>NULL</b>. For 
      more information on the progress callback function, see the 
      <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nc-winbase-lpprogress_routine">CopyProgressRoutine</a> function.


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
      <a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information call 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If <i>lpProgressRoutine</i> returns <b>PROGRESS_CANCEL</b> due to the 
       user canceling the operation, <b>CopyFileTransacted</b> 
       will return zero and <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
       <b>ERROR_REQUEST_ABORTED</b>. In this case, the partially copied destination file is 
       deleted.

If <i>lpProgressRoutine</i> returns <b>PROGRESS_STOP</b> due to the 
       user stopping the operation, <b>CopyFileTransacted</b> 
       will return zero and <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
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




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nc-winbase-lpprogress_routine">CopyProgressRoutine</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-movefiletransacteda">MoveFileTransacted</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
 

 

