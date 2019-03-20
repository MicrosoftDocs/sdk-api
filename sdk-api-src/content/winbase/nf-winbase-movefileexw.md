---
UID: NF:winbase.MoveFileExW
title: MoveFileExW function (winbase.h)
author: windows-sdk-content
description: Moves an existing file or directory, including its children, with various move options.
old-location: fs\movefileex.htm
tech.root: FileIO
ms.assetid: 5fb4f897-66ed-49d7-913a-fb6e7cecdfa3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MOVEFILE_COPY_ALLOWED, MOVEFILE_CREATE_HARDLINK, MOVEFILE_DELAY_UNTIL_REBOOT, MOVEFILE_FAIL_IF_NOT_TRACKABLE, MOVEFILE_REPLACE_EXISTING, MOVEFILE_WRITE_THROUGH, MoveFileEx, MoveFileEx function [Files], MoveFileExA, MoveFileExW, _win32_movefileex, base.movefileex, fs.movefileex, rename file [Files], winbase/MoveFileEx, winbase/MoveFileExA, winbase/MoveFileExW
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MoveFileExW (Unicode) and MoveFileExA (ANSI)
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
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-File-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l2-1-1.dll
 - API-MS-Win-Core-File-l2-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - MoveFileEx
 - MoveFileExA
 - MoveFileExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MoveFileExW function


## -description


Moves an existing file or directory, including its children, with various move options.

The <a href="https://msdn.microsoft.com/f490aadc-7934-498a-8131-5c1be9e6f1aa">MoveFileWithProgress</a> function is equivalent 
    to the <b>MoveFileEx</b> function, except that 
    <b>MoveFileWithProgress</b> allows you to provide a 
    callback function that receives progress notifications.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/466d733b-30d2-4297-a0e6-77038f1a21d5">MoveFileTransacted</a> function.


## -parameters




### -param lpExistingFileName [in]

The current name of the file or directory on the local computer.

If <i>dwFlags</i> specifies <b>MOVEFILE_DELAY_UNTIL_REBOOT</b>, the 
       file cannot exist on a remote share, because delayed operations are performed before the network is 
       available.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>


<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>MoveFileExW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param lpNewFileName [in, optional]

The new name of the file or directory on the local computer.

When moving a file, the destination can be on a different file system or volume. If the destination is on 
       another drive, you must set the <b>MOVEFILE_COPY_ALLOWED</b> flag in 
       <i>dwFlags</i>.

When moving a directory, the destination must be on the same drive.

If <i>dwFlags</i> specifies <b>MOVEFILE_DELAY_UNTIL_REBOOT</b> and 
       <i>lpNewFileName</i> is  <b>NULL</b>, 
       <b>MoveFileEx</b> registers the 
       <i>lpExistingFileName</i> file to be deleted when the system restarts. If 
       <i>lpExistingFileName</i> refers to a directory, the system removes the directory at restart 
       only if the directory is empty.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>


<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>MoveFileExW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param dwFlags [in]

This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MOVEFILE_COPY_ALLOWED"></a><a id="movefile_copy_allowed"></a><dl>
<dt><b>MOVEFILE_COPY_ALLOWED</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
If the file is to be moved to a different volume, the function simulates the move by using the 
        <a href="https://msdn.microsoft.com/2c8ad002-cef4-499c-acda-c162205f6a8d">CopyFile</a> and 
        <a href="https://msdn.microsoft.com/0b947a85-816b-4374-a8f8-c369e366a17d">DeleteFile</a> functions.

If the  file is successfully copied to a different volume and the original file is unable to be deleted, 
         the function succeeds leaving the source file intact.

This value cannot be used with <b>MOVEFILE_DELAY_UNTIL_REBOOT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MOVEFILE_CREATE_HARDLINK"></a><a id="movefile_create_hardlink"></a><dl>
<dt><b>MOVEFILE_CREATE_HARDLINK</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="MOVEFILE_DELAY_UNTIL_REBOOT"></a><a id="movefile_delay_until_reboot"></a><dl>
<dt><b>MOVEFILE_DELAY_UNTIL_REBOOT</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
The system does not move the file until the operating system is restarted. The system moves the file 
        immediately after AUTOCHK is executed, but before creating any paging files. Consequently, this parameter 
        enables the function to delete paging files from previous startups.

This value can be used only if the process is in the context of a user who belongs to the administrators 
         group or the LocalSystem account.
         

This value cannot be used with <b>MOVEFILE_COPY_ALLOWED</b>.

<b>Windows Server 2003 and Windows XP:  </b>For information about special situations where this functionality can fail, and a suggested workaround 
         solution, see 
         <a href="Http://go.microsoft.com/fwlink/p/?linkid=117125">Files are not exchanged when Windows Server 2003 restarts if you use the MoveFileEx function to schedule a replacement for some files</a> 
         in the Help and Support Knowledge Base.

</td>
</tr>
<tr>
<td width="40%"><a id="MOVEFILE_FAIL_IF_NOT_TRACKABLE"></a><a id="movefile_fail_if_not_trackable"></a><dl>
<dt><b>MOVEFILE_FAIL_IF_NOT_TRACKABLE</b></dt>
<dt>32 (0x20)</dt>
</dl>
</td>
<td width="60%">
The function fails if the source file is a link source, but the file cannot be tracked after the move. 
        This situation can occur if the destination is a volume formatted with the FAT file system.

</td>
</tr>
<tr>
<td width="40%"><a id="MOVEFILE_REPLACE_EXISTING"></a><a id="movefile_replace_existing"></a><dl>
<dt><b>MOVEFILE_REPLACE_EXISTING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
If a file named <i>lpNewFileName</i> exists, the function replaces its contents with 
         the contents of the <i>lpExistingFileName</i> file, provided that security requirements 
         regarding access control lists (ACLs) are met. For more information, see the Remarks section of this 
         topic.

This value cannot be used if <i>lpNewFileName</i> or 
         <i>lpExistingFileName</i> names a directory.

</td>
</tr>
<tr>
<td width="40%"><a id="MOVEFILE_WRITE_THROUGH"></a><a id="movefile_write_through"></a><dl>
<dt><b>MOVEFILE_WRITE_THROUGH</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
The function does not return until the file is actually moved on the disk.

Setting this value guarantees that a move performed as a copy and delete operation is flushed to disk 
         before the function returns. The flush occurs at the end of the copy operation.

This value has no effect if <b>MOVEFILE_DELAY_UNTIL_REBOOT</b> is set.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the <i>dwFlags</i> parameter specifies 
     <b>MOVEFILE_DELAY_UNTIL_REBOOT</b>, 
     <b>MoveFileEx</b> fails if it cannot access the registry. The 
     function stores the locations of the files to be renamed at restart in the following registry value:
     <b>HKEY_LOCAL_MACHINE</b>\<b>SYSTEM</b>\<b>CurrentControlSet</b>\<b>Control</b>\<b>Session Manager</b>\<b>PendingFileRenameOperations</b>



This registry  value is of type <b>REG_MULTI_SZ</b>. Each rename operation stores one 
       of the following NULL-terminated strings, depending on whether the rename is a delete or not:

<ul>
<li>
<i>szDstFile</i>\0\0

</li>
<li>
<i>szSrcFile</i>\0<i>szDstFile</i>\0

</li>
</ul>
The string <i>szDstFile</i>\0\0 indicates that the file 
     <i>szDstFile</i> is to be deleted on reboot. The string 
     <i>szSrcFile</i>\0<i>szDstFile</i>\0 indicates that 
     <i>szSrcFile</i> is to be renamed <i>szDstFile</i> on reboot.

<div class="alert"><b>Note</b>  Although \0\0 is technically not allowed in a <b>REG_MULTI_SZ</b> node, it can because 
     the file is considered to be renamed to a null name.</div>
<div> </div>
The system uses these registry entries to complete the operations at restart in the same order that they were 
     issued. For example, the following code fragment creates registry entries that delete 
     <i>szDstFile</i> and rename <i>szSrcFile</i> to be 
     <i>szDstFile</i> at restart:


```cpp
MoveFileEx(szDstFile, NULL, MOVEFILE_DELAY_UNTIL_REBOOT);
MoveFileEx(szSrcFile, szDstFile, MOVEFILE_DELAY_UNTIL_REBOOT);

```


Because the actual move and deletion operations specified with the 
     <b>MOVEFILE_DELAY_UNTIL_REBOOT</b> flag take place after the calling application has ceased 
     running, the return value cannot reflect success or failure in moving or deleting the file. Rather, it reflects 
     success or failure in placing the appropriate entries into the registry.

The system deletes a directory that is tagged for deletion with the 
     <b>MOVEFILE_DELAY_UNTIL_REBOOT</b> flag only if it is empty. To ensure deletion of directories, 
     move or delete all files from the directory before attempting to delete it. Files may be in the directory at boot 
     time, but they must be deleted or moved before the system can delete the directory.

The move and deletion operations are carried out at boot time in the same order that they are specified in the 
     calling application. To delete a directory that has files in it at boot time, first delete the files.

<b>Windows Server 2003 and Windows XP:  </b>For information about special situations where <b>MOVEFILE_DELAY_UNTIL_REBOOT</b> 
     functionality can fail, and a suggested workaround solution, see 
     <a href="Http://go.microsoft.com/fwlink/p/?linkid=117125">Files are not exchanged when Windows Server 2003 restarts if you use the MoveFileEx function to schedule a replacement for some files</a> 
     in the Help and Support Knowledge Base.

If a file is moved across volumes, <b>MoveFileEx</b> does not 
     move the security descriptor with the file. The file is assigned the default security descriptor in the 
     destination directory.

The <b>MoveFileEx</b> function coordinates its operation with 
     the <a href="https://msdn.microsoft.com/6f438c72-f23d-4ca4-83bd-fe3bc433ceeb">link tracking</a> service, 
     so link sources can be tracked as they are moved.

To delete or rename a file, you must have either delete permission on the file or delete child permission in 
     the parent directory. If you set up a directory with all access except delete and delete child and the ACLs of 
     new files are inherited, then you should be able to create a file without being able to delete it. However, you 
     can then create a file, and get all the access you request on the handle that is returned to you at the time that 
     you create the file. If you request delete permission at the time you create the file, you can delete or rename 
     the file with that handle but not with any other handle.  For more information, see 
     <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.

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
      <a href="https://msdn.microsoft.com/6254c67d-5d34-499d-b1a4-8cac526dd294">Creating and Using a Temporary File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2c8ad002-cef4-499c-acda-c162205f6a8d">CopyFile</a>



<a href="https://msdn.microsoft.com/0b947a85-816b-4374-a8f8-c369e366a17d">DeleteFile</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>



<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a>



<a href="https://msdn.microsoft.com/466d733b-30d2-4297-a0e6-77038f1a21d5">MoveFileTransacted</a>



<a href="https://msdn.microsoft.com/f490aadc-7934-498a-8131-5c1be9e6f1aa">MoveFileWithProgress</a>



<a href="https://msdn.microsoft.com/f0799092-c6c1-4800-a17a-fcf744b1228f">WritePrivateProfileString</a>
 

 

