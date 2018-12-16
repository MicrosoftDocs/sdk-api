---
UID: NF:fileapi.FindFirstChangeNotificationW
title: FindFirstChangeNotificationW function
author: windows-sdk-content
description: Creates a change notification handle and sets up initial change notification filter conditions.
old-location: fs\findfirstchangenotification.htm
tech.root: fileio
ms.assetid: dde4dd17-0f8c-41b5-8685-4e4c6b3def3c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FILE_NOTIFY_CHANGE_ATTRIBUTES, FILE_NOTIFY_CHANGE_DIR_NAME, FILE_NOTIFY_CHANGE_FILE_NAME, FILE_NOTIFY_CHANGE_LAST_WRITE, FILE_NOTIFY_CHANGE_SECURITY, FILE_NOTIFY_CHANGE_SIZE, FindFirstChangeNotification, FindFirstChangeNotification function [Files], FindFirstChangeNotificationA, FindFirstChangeNotificationW, _win32_findfirstchangenotification, base.findfirstchangenotification, fileapi/FindFirstChangeNotification, fileapi/FindFirstChangeNotificationA, fileapi/FindFirstChangeNotificationW, fs.findfirstchangenotification, winbase/FindFirstChangeNotification, winbase/FindFirstChangeNotificationA, winbase/FindFirstChangeNotificationW
ms.topic: function
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
 - FindFirstChangeNotification
 - FindFirstChangeNotificationA
 - FindFirstChangeNotificationW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindFirstChangeNotificationW function


## -description


Creates a change notification handle and sets up initial change notification filter conditions. A wait on a notification handle succeeds when a change matching the filter conditions occurs in the specified directory or subtree. The function does not report changes to the specified directory itself.

This function does not indicate the change that satisfied the wait condition. To retrieve information about the specific change as part of the notification, use the  
<a href="https://msdn.microsoft.com/14dfc93d-557e-43d0-be45-8414cfd92c29">ReadDirectoryChangesW</a> function.


## -parameters




### -param lpPathName [in]

The full path of the directory to be watched. 


This cannot be a relative path or an empty string.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend "\\?\" to the path. For more information, see 
<a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.


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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a> can monitor the specified directory or subtree by using the handle returned by the 
<b>FindFirstChangeNotification</b> function. A wait is satisfied when one of the filter conditions occurs in the monitored directory or subtree.

After the wait has been satisfied, the application can respond to this condition and continue monitoring the directory by calling the 
<a href="https://msdn.microsoft.com/0f93cc96-6e3b-4c03-aa5a-7a74d054a7ff">FindNextChangeNotification</a> function and the appropriate wait function. When the handle is no longer needed, it can be closed by using the 
<a href="https://msdn.microsoft.com/17ca915c-3891-41f0-8816-6ac31c957afe">FindCloseChangeNotification</a> function.

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
<a href="https://msdn.microsoft.com/ad884b15-e040-478b-aa99-d8622198f62a">Obtaining Directory Change_Notifications</a>.
				

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5517b0e7-2264-4173-8e10-ff7626458bfa">Directory Management Functions</a>



<a href="https://msdn.microsoft.com/17ca915c-3891-41f0-8816-6ac31c957afe">FindCloseChangeNotification</a>



<a href="https://msdn.microsoft.com/0f93cc96-6e3b-4c03-aa5a-7a74d054a7ff">FindNextChangeNotification</a>



<a href="https://msdn.microsoft.com/14dfc93d-557e-43d0-be45-8414cfd92c29">ReadDirectoryChangesW</a>
 

 

