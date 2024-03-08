---
UID: NF:winbase.DeleteFile
title: DeleteFile function (winbase.h)
description: The DeleteFile function (winbase.h) deletes an existing file.
helpviewer_keywords: ["DeleteFile","DeleteFile function [Files]","DeleteFileA","DeleteFileW","_win32_deletefile","base.deletefile","fileapi/DeleteFile","fileapi/DeleteFileA","fileapi/DeleteFileW","fs.deletefile","winbase/DeleteFile","winbase/DeleteFileA","winbase/DeleteFileW"]
old-location: fs\deletefile.htm
tech.root: fs
ms.assetid: 0b947a85-816b-4374-a8f8-c369e366a17d
ms.date: 08/04/2022
ms.keywords: DeleteFile, DeleteFile function [Files], DeleteFileA, DeleteFileW, _win32_deletefile, base.deletefile, fileapi/DeleteFile, fileapi/DeleteFileA, fileapi/DeleteFileW, fs.deletefile, winbase/DeleteFile, winbase/DeleteFileA, winbase/DeleteFileW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteFileW (Unicode) and DeleteFileA (ANSI)
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
 - DeleteFile
 - winbase/DeleteFile
dev_langs:
 - c++
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
---

# DeleteFile function


## -description

Deletes an existing file.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-deletefiletransacteda">DeleteFileTransacted</a> function.

## -parameters

### -param lpFileName [in]

The name of the file to be deleted.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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
     <a href="/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> function.</li>
<li>To remove an empty directory, use the 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-removedirectorya">RemoveDirectory</a> function.</li>
<li>To close an open file, use the 
     <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.</li>
</ul>
If you set up a directory with all access except delete and delete child, and the access control lists (ACL) of 
     new files are inherited, then you can create a file without being able to delete it. However, then you can create 
     a file, and then get all the access you request on the handle that is returned to you at the time you create the 
     file.

If you request delete permission at the time you create a file, you can delete or rename the file with that 
     handle, but not with any other handle. For more information, see 
     <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

The <b>DeleteFile</b> function fails if an application attempts 
    to delete a file that has other handles open for normal I/O or as a memory-mapped file 
    (<b>FILE_SHARE_DELETE</b> must have been specified when other handles were opened).

The <b>DeleteFile</b> function marks a file for deletion on 
    close. Therefore, the file deletion does not occur until the last handle to the file is closed. Subsequent calls 
    to <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> to open the file fail with 
    <b>ERROR_ACCESS_DENIED</b>.

Symbolic link behavior—

If the path points to a symbolic link, the symbolic link is deleted, not the target. To delete a target, you 
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
     <a href="/windows/desktop/FileIO/locking-and-unlocking-byte-ranges-in-files">Locking and Unlocking Byte Ranges in Files</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deletefiletransacteda">DeleteFileTransacted</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>
