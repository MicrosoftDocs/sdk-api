---
UID: NF:winbase.MoveFileTransactedW
title: MoveFileTransactedW function (winbase.h)
description: Moves an existing file or a directory, including its children, as a transacted operation. (Unicode)
old-location: fs\movefiletransacted.htm
tech.root: FileIO
ms.assetid: 466d733b-30d2-4297-a0e6-77038f1a21d5
ms.date: 12/05/2018
ms.keywords: MOVEFILE_COPY_ALLOWED, MOVEFILE_CREATE_HARDLINK, MOVEFILE_DELAY_UNTIL_REBOOT, MOVEFILE_REPLACE_EXISTING, MOVEFILE_WRITE_THROUGH, MoveFileTransacted, MoveFileTransacted function [Files], MoveFileTransactedA, MoveFileTransactedW, fs.movefiletransacted, rename file [Files], winbase/MoveFileTransacted, winbase/MoveFileTransactedA, winbase/MoveFileTransactedW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MoveFileTransactedW
 - winbase/MoveFileTransactedW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
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
---

# MoveFileTransactedW function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Moves an existing file or a directory, including its children, as a transacted 
    operation.

## -parameters

### -param lpExistingFileName [in]

The current name of the existing file or directory on the local computer.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpNewFileName [in, optional]

The new name for the file or directory. The new name must not already exist. A new file may be on a 
      different file system or drive. A new directory must be on the same drive.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpProgressRoutine [in, optional]

A pointer to a <a href="/windows/desktop/api/winbase/nc-winbase-lpprogress_routine">CopyProgressRoutine</a> callback 
      function that is called each time another portion of the file has been moved. The callback function can be 
      useful if you provide a user interface that displays the progress of the operation. This parameter can be 
      <b>NULL</b>.

### -param lpData [in, optional]

An argument to be passed to the 
      <a href="/windows/desktop/api/winbase/nc-winbase-lpprogress_routine">CopyProgressRoutine</a> callback function. This 
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
         <a href="/windows/desktop/api/winbase/nf-winbase-copyfile">CopyFile</a> and 
         <a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a> functions.

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
      <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

When moving a file across volumes, if <i>lpProgressRoutine</i> returns 
       <b>PROGRESS_CANCEL</b> due to the user canceling the operation, 
       <b>MoveFileTransacted</b> will return zero and 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
       <b>ERROR_REQUEST_ABORTED</b>. The existing file is left intact.

When moving a file across volumes, if <i>lpProgressRoutine</i> returns 
       <b>PROGRESS_STOP</b> due to the user stopping the operation, 
       <b>MoveFileTransacted</b> will return zero and 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
       <b>ERROR_REQUEST_ABORTED</b>. The existing file is left intact.

## -remarks

If the <i>dwFlags</i> parameter specifies 
    <b>MOVEFILE_DELAY_UNTIL_REBOOT</b>, 
    <b>MoveFileTransacted</b> fails if it cannot access the registry. The 
    function transactionally stores the locations of the files to be renamed at restart in the following registry 
    value:
    <b>HKEY_LOCAL_MACHINE</b>&#92;<b>SYSTEM</b>&#92;<b>CurrentControlSet</b>&#92;<b>Control</b>&#92;<b>Session Manager</b>&#92;<b>PendingFileRenameOperations</b>



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
    <a href="/windows/desktop/api/winbase/nf-winbase-movefilewithprogressa">MoveFileWithProgress</a>.

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

<a href="/windows/desktop/api/winbase/nf-winbase-copyfiletransacteda">CopyFileTransacted</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefilewithprogressa">MoveFileWithProgress</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
