---
UID: NF:winbase.MoveFileWithProgressA
title: MoveFileWithProgressA function (winbase.h)
description: Moves a file or directory, including its children. You can provide a callback function that receives progress notifications. (ANSI)
helpviewer_keywords: ["MOVEFILE_COPY_ALLOWED", "MOVEFILE_CREATE_HARDLINK", "MOVEFILE_DELAY_UNTIL_REBOOT", "MOVEFILE_FAIL_IF_NOT_TRACKABLE", "MOVEFILE_REPLACE_EXISTING", "MOVEFILE_WRITE_THROUGH", "MoveFileWithProgressA", "Rename file [Files]", "winbase/MoveFileWithProgressA"]
old-location: fs\movefilewithprogress.htm
tech.root: fs
ms.assetid: f490aadc-7934-498a-8131-5c1be9e6f1aa
ms.date: 12/05/2018
ms.keywords: MOVEFILE_COPY_ALLOWED, MOVEFILE_CREATE_HARDLINK, MOVEFILE_DELAY_UNTIL_REBOOT, MOVEFILE_FAIL_IF_NOT_TRACKABLE, MOVEFILE_REPLACE_EXISTING, MOVEFILE_WRITE_THROUGH, MoveFileWithProgress, MoveFileWithProgress function [Files], MoveFileWithProgressA, MoveFileWithProgressW, Rename file [Files], _win32_movefilewithprogress, base.movefilewithprogress, fs.movefilewithprogress, winbase/MoveFileWithProgress, winbase/MoveFileWithProgressA, winbase/MoveFileWithProgressW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MoveFileWithProgressW (Unicode) and MoveFileWithProgressA (ANSI)
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
 - MoveFileWithProgressA
 - winbase/MoveFileWithProgressA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-File-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l2-1-1.dll
 - API-MS-Win-Core-File-l2-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - API-Ms-Win-Core-File-Ansi-L2-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - MoveFileWithProgress
 - MoveFileWithProgressA
 - MoveFileWithProgressW
---

# MoveFileWithProgressA function


## -description

Moves a file or directory, including its children. You can provide a callback function that receives 
    progress notifications.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-movefiletransacteda">MoveFileTransacted</a> function.

## -parameters

### -param lpExistingFileName [in]

The name of the existing file or directory on the local computer.

If <i>dwFlags</i> specifies <b>MOVEFILE_DELAY_UNTIL_REBOOT</b>, the 
       file cannot exist on a remote share because delayed operations are performed before the network is 
       available.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpNewFileName [in, optional]

The new name of the file or directory  on the local computer.

When moving a file, <i>lpNewFileName</i> can be on a different file system or volume. If 
       <i>lpNewFileName</i> is on another drive, you must set the 
       <b>MOVEFILE_COPY_ALLOWED</b> flag in <i>dwFlags</i>.

When moving a directory, <i>lpExistingFileName</i> and 
       <i>lpNewFileName</i> must be on the same drive.

If <i>dwFlags</i> specifies <b>MOVEFILE_DELAY_UNTIL_REBOOT</b> and 
       <i>lpNewFileName</i> is <b>NULL</b>, 
       <b>MoveFileWithProgress</b> registers 
       <i>lpExistingFileName</i> to be deleted when the system restarts. The function fails if it 
       cannot access the registry to store the information about the delete operation. If 
       <i>lpExistingFileName</i> refers to a directory, the system removes the directory at restart 
       only if the directory is empty.

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
         the contents of the <i>lpExistingFileName</i> file.

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
The function does not return until the file has actually been moved on the disk.

Setting this value guarantees that a move performed as a copy and delete operation is flushed to disk 
         before the function returns. The flush occurs at the end of the copy operation.

This value has no effect if <b>MOVEFILE_DELAY_UNTIL_REBOOT</b> is set.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

When moving a file across volumes, if <i>lpProgressRoutine</i> returns 
       <b>PROGRESS_CANCEL</b> due to the user canceling the operation, 
       <b>MoveFileWithProgress</b> will return zero and 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
       <b>ERROR_REQUEST_ABORTED</b>. The existing file is left intact.

When moving a file across volumes, if <i>lpProgressRoutine</i> returns 
       <b>PROGRESS_STOP</b> due to the user stopping the operation, 
       <b>MoveFileWithProgress</b> will return zero and 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
       <b>ERROR_REQUEST_ABORTED</b>. The existing file is left intact.

## -remarks

The <b>MoveFileWithProgress</b> function coordinates its operation with the link 
    tracking service, so link sources can be tracked as they are moved.

To delete or rename a file, you must have either delete permission on the file or delete child permission in 
    the parent directory. If you set up a directory with all access except delete and delete child and the ACLs of new 
    files are inherited, then you should be able to create a file without being able to delete it. However, you can 
    then create a file, and you will get all the access you request on the handle returned to you at the time you 
    create the file. If you requested delete permission at the time you created the file, you could delete or rename 
    the file with that handle but not with any other.

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
 

CsvFs will do redirected IO for compressed files.






> [!NOTE]
> The winbase.h header defines MoveFileWithProgress as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-copyfileexa">CopyFileEx</a>



<a href="/windows/desktop/api/winbase/nc-winbase-lpprogress_routine">CopyProgressRoutine</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefileexa">MoveFileEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefiletransacteda">MoveFileTransacted</a>
