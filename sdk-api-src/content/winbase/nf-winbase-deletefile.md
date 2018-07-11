---
UID: NF:winbase.DeleteFile
title: DeleteFile function
author: windows-sdk-content
description: Deletes an existing file.
old-location: fs\deletefile.htm
old-project: fileio
ms.assetid: 0b947a85-816b-4374-a8f8-c369e366a17d
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: DeleteFile, DeleteFile function [Files], DeleteFileA, DeleteFileW, _win32_deletefile, base.deletefile, fileapi/DeleteFile, fileapi/DeleteFileA, fileapi/DeleteFileW, fs.deletefile, winbase/DeleteFile, winbase/DeleteFileA, winbase/DeleteFileW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteFileW (Unicode) and DeleteFileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - DeleteFile
 - DeleteFileA
 - DeleteFileW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DeleteFile function


## -description


Deletes an existing file.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/e0a6230b-2da1-4746-95fe-80f7b6bae41f">DeleteFileTransacted</a> function.


## -parameters




### -param lpFileName [in]

The name of the file to be deleted.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting in Windows 10, version 1607, for the unicode version of this function (<b>DeleteFileW</b>), you can opt-in to remove the <b>MAX_PATH</b> character limitation without prepending "\\?\". See the "Maximum Path Limitation" section of  <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details. </div>
<div> </div>

## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If an application attempts to delete a file that does not exist, the 
    <b>DeleteFile</b> function fails with 
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
     <a href="https://msdn.microsoft.com/d699cdd2-e270-4f17-bdec-6eea25b01578">RemoveDirectory</a> function.</li>
<li>To close an open file, use the 
     <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.</li>
</ul>
If you set up a directory with all access except delete and delete child, and the access control lists (ACL) of 
     new files are inherited, then you can create a file without being able to delete it. However, then you can create 
     a file, and then get all the access you request on the handle that is returned to you at the time you create the 
     file.

If you request delete permission at the time you create a file, you can delete or rename the file with that 
     handle, but not with any other handle. For more information, see 
     <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.

The <b>DeleteFile</b> function fails if an application attempts 
    to delete a file that has other handles open for normal I/O or as a memory-mapped file 
    (<b>FILE_SHARE_DELETE</b> must have been specified when other handles were opened).

The <b>DeleteFile</b> function marks a file for deletion on 
    close. Therefore, the file deletion does not occur until the last handle to the file is closed. Subsequent calls 
    to <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> to open the file fail with 
    <b>ERROR_ACCESS_DENIED</b>.

Symbolic link behavior—

If the path points to a symbolic link, the symbolic link is deleted, not the target. To delete a target, you 
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
 


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/9d54fe11-b1ad-4723-a42a-00bc6dc64072">Locking and Unlocking Byte Ranges in Files</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/e0a6230b-2da1-4746-95fe-80f7b6bae41f">DeleteFileTransacted</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>
 

 

