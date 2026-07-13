---
UID: NF:winbase.DeleteFileTransactedA
title: DeleteFileTransactedA function (winbase.h)
description: Deletes an existing file as a transacted operation. (ANSI)
helpviewer_keywords: ["DeleteFileTransactedA", "winbase/DeleteFileTransactedA"]
old-location: fs\deletefiletransacted.htm
tech.root: fs
ms.assetid: e0a6230b-2da1-4746-95fe-80f7b6bae41f
ms.date: 12/05/2018
ms.keywords: DeleteFileTransacted, DeleteFileTransacted function [Files], DeleteFileTransactedA, DeleteFileTransactedW, fs.deletefiletransacted, winbase/DeleteFileTransacted, winbase/DeleteFileTransactedA, winbase/DeleteFileTransactedW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteFileTransactedW (Unicode) and DeleteFileTransactedA (ANSI)
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
 - DeleteFileTransactedA
 - winbase/DeleteFileTransactedA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - Ext-MS-Win-Kernel32-Transacted-l1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - DeleteFileTransacted
 - DeleteFileTransactedA
 - DeleteFileTransactedW
---

# DeleteFileTransactedA function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Deletes an existing file as a transacted operation.

## -parameters

### -param lpFileName [in]

The name of the file to be deleted.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to 
       <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If an application attempts to delete a file that does not exist, the 
    <b>DeleteFileTransacted</b> function fails with 
    <b>ERROR_FILE_NOT_FOUND</b>. If the file is a read-only file, the function fails with 
    <b>ERROR_ACCESS_DENIED</b>.

The following list identifies some tips for deleting, removing, or closing files:

<ul>
<li>To delete a read-only file, first you must remove the read-only attribute.</li>
<li>To delete or rename a file, you must have either delete permission on the file, or delete child permission 
      in the parent directory.</li>
<li>To recursively delete the files in a directory, use the 
      <a href="/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> function.</li>
<li>To remove an empty directory, use the 
      <a href="/windows/desktop/api/winbase/nf-winbase-removedirectorytransacteda">RemoveDirectoryTransacted</a> function.</li>
<li>To close an open file, use the 
      <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.</li>
</ul>
If you set up a directory with all access except delete and delete child, and the access control lists (ACL) 
      of new files are inherited, then you can create a file without being able to delete it. However, then you can 
      create a file, and then get all the access you request on the handle that is returned to you at the time you 
      create the file.

If you request delete permission at the time you create a file, you can delete or rename the file with that 
      handle, but not with any other handle. For more information, see 
      <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

The <b>DeleteFileTransacted</b> function fails if an 
    application attempts to delete a file that has other handles open for normal I/O or as a memory-mapped file 
    (<b>FILE_SHARE_DELETE</b> must have been specified when other handles were opened).

The <b>DeleteFileTransacted</b> function marks a file 
    for deletion on close. The file is deleted after the last transacted writer handle to the file is closed, provided 
    that the transaction is still active. If a file has been marked for deletion and a transacted writer handle is 
    still open after the transaction completes, the file will not be deleted.

<b>Symbolic links:  </b>If the path points to a symbolic link, the symbolic link is deleted, not the target. To delete a target, you 
      must call <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> and specify 
      <b>FILE_FLAG_DELETE_ON_CLOSE</b>.

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
> The winbase.h header defines DeleteFileTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
