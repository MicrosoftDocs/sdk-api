---
UID: NF:winbase.DeleteFileTransactedW
title: DeleteFileTransactedW function
author: windows-sdk-content
description: Deletes an existing file as a transacted operation.
old-location: fs\deletefiletransacted.htm
old-project: FileIO
ms.assetid: e0a6230b-2da1-4746-95fe-80f7b6bae41f
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: DeleteFileTransacted, DeleteFileTransacted function [Files], DeleteFileTransactedA, DeleteFileTransactedW, fs.deletefiletransacted, winbase/DeleteFileTransacted, winbase/DeleteFileTransactedA, winbase/DeleteFileTransactedW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	Ext-MS-Win-Kernel32-Transacted-l1-1-0.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	Kernel32Legacy.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
-	DeleteFileTransacted
-	DeleteFileTransactedA
-	DeleteFileTransactedW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DeleteFileTransactedW function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Deletes an existing file as a transacted operation.


## -parameters




### -param lpFileName [in]

The name of the file to be deleted.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to 
       <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.


### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




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
      <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a> function.</li>
<li>To remove an empty directory, use the 
      <a href="https://msdn.microsoft.com/e8600166-62dc-4398-9e16-43b07f7f0b89">RemoveDirectoryTransacted</a> function.</li>
<li>To close an open file, use the 
      <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.</li>
</ul>
If you set up a directory with all access except delete and delete child, and the access control lists (ACL) 
      of new files are inherited, then you can create a file without being able to delete it. However, then you can 
      create a file, and then get all the access you request on the handle that is returned to you at the time you 
      create the file.

If you request delete permission at the time you create a file, you can delete or rename the file with that 
      handle, but not with any other handle. For more information, see 
      <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.

The <b>DeleteFileTransacted</b> function fails if an 
    application attempts to delete a file that has other handles open for normal I/O or as a memory-mapped file 
    (<b>FILE_SHARE_DELETE</b> must have been specified when other handles were opened).

The <b>DeleteFileTransacted</b> function marks a file 
    for deletion on close. The file is deleted after the last transacted writer handle to the file is closed, provided 
    that the transaction is still active. If a file has been marked for deletion and a transacted writer handle is 
    still open after the transaction completes, the file will not be deleted.

<b>Symbolic links:  </b>If the path points to a symbolic link, the symbolic link is deleted, not the target. To delete a target, you 
      must call <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> and specify 
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




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/0cbc081d-8787-409b-84bc-a6a28d8f83a0">CreateFileTransacted</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>
 

 

