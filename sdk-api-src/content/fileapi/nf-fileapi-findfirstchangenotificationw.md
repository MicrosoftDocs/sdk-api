---
UID: NF:fileapi.FindFirstChangeNotificationW
title: FindFirstChangeNotificationW function (fileapi.h)
description: Creates a change notification handle and sets up initial change notification filter conditions. (Unicode)
helpviewer_keywords: ["FILE_NOTIFY_CHANGE_ATTRIBUTES", "FILE_NOTIFY_CHANGE_DIR_NAME", "FILE_NOTIFY_CHANGE_FILE_NAME", "FILE_NOTIFY_CHANGE_LAST_WRITE", "FILE_NOTIFY_CHANGE_SECURITY", "FILE_NOTIFY_CHANGE_SIZE", "FindFirstChangeNotification", "FindFirstChangeNotification function [Files]", "FindFirstChangeNotificationW", "_win32_findfirstchangenotification", "base.findfirstchangenotification", "fileapi/FindFirstChangeNotification", "fileapi/FindFirstChangeNotificationW", "fs.findfirstchangenotification"]
old-location: fs\findfirstchangenotification.htm
tech.root: fs
ms.assetid: dde4dd17-0f8c-41b5-8685-4e4c6b3def3c
ms.date: 12/05/2018
ms.keywords: FILE_NOTIFY_CHANGE_ATTRIBUTES, FILE_NOTIFY_CHANGE_DIR_NAME, FILE_NOTIFY_CHANGE_FILE_NAME, FILE_NOTIFY_CHANGE_LAST_WRITE, FILE_NOTIFY_CHANGE_SECURITY, FILE_NOTIFY_CHANGE_SIZE, FindFirstChangeNotification, FindFirstChangeNotification function [Files], FindFirstChangeNotificationA, FindFirstChangeNotificationW, _win32_findfirstchangenotification, base.findfirstchangenotification, fileapi/FindFirstChangeNotification, fileapi/FindFirstChangeNotificationA, fileapi/FindFirstChangeNotificationW, fs.findfirstchangenotification, winbase/FindFirstChangeNotification, winbase/FindFirstChangeNotificationA, winbase/FindFirstChangeNotificationW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindFirstChangeNotificationW (Unicode) and FindFirstChangeNotificationA (ANSI)
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
 - FindFirstChangeNotificationW
 - fileapi/FindFirstChangeNotificationW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - FindFirstChangeNotification
 - FindFirstChangeNotificationA
 - FindFirstChangeNotificationW
---

# FindFirstChangeNotificationW function


## -description

Creates a change notification handle and sets up initial change notification filter conditions. A wait on a notification handle succeeds when a change matching the filter conditions occurs in the specified directory or subtree. The function does not report changes to the specified directory itself.

This function does not indicate the change that satisfied the wait condition. To retrieve information about the specific change as part of the notification, use the  
<a href="/windows/desktop/api/winbase/nf-winbase-readdirectorychangesw">ReadDirectoryChangesW</a> function.

## -parameters

### -param lpPathName [in]

The full path of the directory to be watched. 


This cannot be a relative path or an empty string.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.
### -param bWatchSubtree [in]

If this parameter is <b>TRUE</b>, the function monitors the directory tree rooted at the specified directory; if it is <b>FALSE</b>, it monitors only the specified directory.

### -param dwNotifyFilter [in]

The filter conditions that satisfy a change notification wait. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_FILE_NAME"></a><a id="file_notify_change_file_name"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_FILE_NAME</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Any file name change in the watched directory or subtree causes a change notification wait operation to return. Changes include renaming, creating, or deleting a file name.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_DIR_NAME"></a><a id="file_notify_change_dir_name"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_DIR_NAME</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Any directory-name change in the watched directory or subtree causes a change notification wait operation to return. Changes include creating or deleting a directory.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_ATTRIBUTES"></a><a id="file_notify_change_attributes"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_ATTRIBUTES</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Any attribute change in the watched directory or subtree causes a change notification wait operation to return.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_SIZE"></a><a id="file_notify_change_size"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_SIZE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Any file-size change in the watched directory or subtree causes a change notification wait operation to return. The operating system detects a change in file size only when the file is written to the disk. For operating systems that use extensive caching, detection occurs only when the cache is sufficiently flushed.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_LAST_WRITE"></a><a id="file_notify_change_last_write"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_LAST_WRITE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Any change to the last write-time of files in the watched directory or subtree causes a change notification wait operation to return. The operating system detects a change to the last write-time only when the file is written to the disk. For operating systems that use extensive caching, detection occurs only when the cache is sufficiently flushed.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_SECURITY"></a><a id="file_notify_change_security"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_SECURITY</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Any security-descriptor change in the watched directory or subtree causes a change notification wait operation to return.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a handle to a find change notification object.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a> can monitor the specified directory or subtree by using the handle returned by the 
<b>FindFirstChangeNotification</b> function. A wait is satisfied when one of the filter conditions occurs in the monitored directory or subtree.

After the wait has been satisfied, the application can respond to this condition and continue monitoring the directory by calling the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextchangenotification">FindNextChangeNotification</a> function and the appropriate wait function. When the handle is no longer needed, it can be closed by using the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-findclosechangenotification">FindCloseChangeNotification</a> function.

Notifications may not be returned when calling <b>FindFirstChangeNotification</b> for a remote file system. 

Symbolic link behavior—If the path points to a symbolic link, the notification handle is created for the target.

If an application has registered to receive change notifications for a directory that contains symbolic links, the application is only notified when the symbolic links have been changed, not the target files.

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
See remark

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
 

Application might experience false positives on CsvFs pause/resume.


#### Examples

For an example, see 
<a href="/windows/desktop/FileIO/obtaining-directory-change-notifications">Obtaining Directory Change_Notifications</a>.
				

<div class="code"></div>




> [!NOTE]
> The fileapi.h header defines FindFirstChangeNotification as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findclosechangenotification">FindCloseChangeNotification</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextchangenotification">FindNextChangeNotification</a>



<a href="/windows/desktop/api/winbase/nf-winbase-readdirectorychangesw">ReadDirectoryChangesW</a>
