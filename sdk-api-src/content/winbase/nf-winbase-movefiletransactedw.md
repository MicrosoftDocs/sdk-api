---
UID: NF:winbase.MoveFileTransactedW
title: MoveFileTransactedW function
author: windows-sdk-content
description: Moves an existing file or a directory, including its children, as a transacted operation.
old-location: fs\movefiletransacted.htm
tech.root: FileIO
ms.assetid: 466d733b-30d2-4297-a0e6-77038f1a21d5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: MOVEFILE_COPY_ALLOWED, MOVEFILE_CREATE_HARDLINK, MOVEFILE_DELAY_UNTIL_REBOOT, MOVEFILE_REPLACE_EXISTING, MOVEFILE_WRITE_THROUGH, MoveFileTransacted, MoveFileTransacted function [Files], MoveFileTransactedA, MoveFileTransactedW, fs.movefiletransacted, rename file [Files], winbase/MoveFileTransacted, winbase/MoveFileTransactedA, winbase/MoveFileTransactedW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MoveFileTransactedW (Unicode) and MoveFileTransactedA (ANSI)
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
 - Ext-MS-Win-Kernel32-Transacted-l1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - MoveFileTransacted
 - MoveFileTransactedA
 - MoveFileTransactedW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MoveFileTransactedW function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Moves an existing file or a directory, including its children, as a transacted 
    operation.


## -parameters




### -param lpExistingFileName [in]

The current name of the existing file or directory on the local computer.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.


### -param lpNewFileName [in, optional]

The new name for the file or directory. The new name must not already exist. A new file may be on a 
      different file system or drive. A new directory must be on the same drive.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.


### -param lpProgressRoutine [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/2c02b212-d4ac-4b01-8955-2561d8c42b1b">CopyProgressRoutine</a> callback 
      function that is called each time another portion of the file has been moved. The callback function can be 
      useful if you provide a user interface that displays the progress of the operation. This parameter can be 
      <b>NULL</b>.


### -param lpData [in, optional]

An argument to be passed to the 
      <a href="https://msdn.microsoft.com/2c02b212-d4ac-4b01-8955-2561d8c42b1b">CopyProgressRoutine</a> callback function. This 
      parameter can be <b>NULL</b>.


### -param dwFlags [in]

The move options. This parameter can be one or more of the following values.

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

This value can only be used if the process is in the context of a user who belongs to the administrators 
         group or the LocalSystem account.

This value cannot be used with <b>MOVEFILE_COPY_ALLOWED</b>.

The write operation to the registry value as detailed in the Remarks section is what is transacted. The 
         file move is finished when the computer restarts, after the transaction is complete.

</td>
</tr>
<tr>
<td width="40%"><a id="MOVEFILE_REPLACE_EXISTING"></a><a id="movefile_replace_existing"></a><dl>
<dt><b>MOVEFILE_REPLACE_EXISTING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
If a file named <i>lpNewFileName</i> exists, the function replaces its contents with the 
         contents of the <i>lpExistingFileName</i> file.

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
A call to <b>MoveFileTransacted</b> means that the 
        move file operation is complete when the commit operation is completed. This flag is unnecessary; there are no 
        negative affects if this flag is specified, other than an operation slowdown. The function does not return 
        until the file has actually been moved on the disk.

Setting this value guarantees that a move performed as a copy and delete operation is flushed to disk 
         before the function returns. The flush occurs at the end of the copy operation.

This value has no effect if <b>MOVEFILE_DELAY_UNTIL_REBOOT</b> is set.

</td>
</tr>
</table>
 


### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

When moving a file across volumes, if <i>lpProgressRoutine</i> returns 
       <b>PROGRESS_CANCEL</b> due to the user canceling the operation, 
       <b>MoveFileTransacted</b> will return zero and 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return 
       <b>ERROR_REQUEST_ABORTED</b>. The existing file is left intact.

When moving a file across volumes, if <i>lpProgressRoutine</i> returns 
       <b>PROGRESS_STOP</b> due to the user stopping the operation, 
       <b>MoveFileTransacted</b> will return zero and 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return 
       <b>ERROR_REQUEST_ABORTED</b>. The existing file is left intact.




## -remarks



If the <i>dwFlags</i> parameter specifies 
    <b>MOVEFILE_DELAY_UNTIL_REBOOT</b>, 
    <b>MoveFileTransacted</b> fails if it cannot access the registry. The 
    function transactionally stores the locations of the files to be renamed at restart in the following registry 
    value:
    <b>HKEY_LOCAL_MACHINE</b>\<b>SYSTEM</b>\<b>CurrentControlSet</b>\<b>Control</b>\<b>Session Manager</b>\<b>PendingFileRenameOperations</b>



This registry  value is of type <b>REG_MULTI_SZ</b>. Each rename operation stores one of 
    the following <b>NULL</b>-terminated strings, depending on whether the rename is a delete or 
    not:

<i>szDstFile</i>\0\0

<i>szSrcFile</i>\0<i>szDstFile</i>\0

The string <i>szDstFile</i>\0\0 indicates that the file 
     <i>szDstFile</i> is to be deleted on reboot.

The string <i>szSrcFile</i>\0<i>szDstFile</i>\0 indicates that 
     <i>szSrcFile</i> is to be renamed <i>szDstFile</i> on reboot.

<div class="alert"><b>Note</b>  Although \0\0 is technically not allowed in a <b>REG_MULTI_SZ</b> node, it can because 
     the file is considered to be renamed to a null name.</div>
<div> </div>
The system uses these registry entries to complete the operations at restart in the same order that they were 
    issued. For more information about using the <b>MOVEFILE_DELAY_UNTIL_REBOOT</b> flag, see 
    <a href="https://msdn.microsoft.com/f490aadc-7934-498a-8131-5c1be9e6f1aa">MoveFileWithProgress</a>.

 If a file is moved across volumes, 
    <b>MoveFileTransacted</b> does not move the security 
    descriptor with the file. The file is assigned the default security descriptor in the destination directory.

This function always fails if you specify the <b>MOVEFILE_FAIL_IF_NOT_TRACKABLE</b> flag; 
    tracking is not supported by TxF.

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




<a href="https://msdn.microsoft.com/118392de-166b-413e-99c9-b3deb756de0e">CopyFileTransacted</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/f490aadc-7934-498a-8131-5c1be9e6f1aa">MoveFileWithProgress</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>
 

 

