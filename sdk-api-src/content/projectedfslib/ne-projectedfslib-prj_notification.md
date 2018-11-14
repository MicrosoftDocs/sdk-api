---
UID: NE:projectedfslib.PRJ_NOTIFICATION
title: PRJ_NOTIFICATION
author: windows-sdk-content
description: A notification value specified when sending the notification in a callback.
old-location: projfs\prj_notification.htm
tech.root: ProjFS
ms.assetid: A1DC0CAF-0101-4410-86A6-5839A8C20988
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: PRJ_NOTIFICATION, PRJ_NOTIFICATION enumeration, PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED, PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_MODIFIED, PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION, PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_FILE_OVERWRITTEN, PRJ_NOTIFICATION_FILE_RENAMED, PRJ_NOTIFICATION_HARDLINK_CREATED, PRJ_NOTIFICATION_NEW_FILE_CREATED, PRJ_NOTIFICATION_PRE_CONVERT_TO_FULL, PRJ_NOTIFICATION_PRE_DELETE, PRJ_NOTIFICATION_PRE_RENAME, PRJ_NOTIFICATION_PRE_SET_HARDLINK, ProjFS.prj_notification, projectedfslib/PRJ_NOTIFICATION, projectedfslib/PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED, projectedfslib/PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_MODIFIED, projectedfslib/PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION, projectedfslib/PRJ_NOTIFICATION_FILE_OPENED, projectedfslib/PRJ_NOTIFICATION_FILE_OVERWRITTEN, projectedfslib/PRJ_NOTIFICATION_FILE_RENAMED, projectedfslib/PRJ_NOTIFICATION_HARDLINK_CREATED, projectedfslib/PRJ_NOTIFICATION_NEW_FILE_CREATED, projectedfslib/PRJ_NOTIFICATION_PRE_CONVERT_TO_FULL, projectedfslib/PRJ_NOTIFICATION_PRE_DELETE, projectedfslib/PRJ_NOTIFICATION_PRE_RENAME, projectedfslib/PRJ_NOTIFICATION_PRE_SET_HARDLINK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ProjectedFSLib.h
api_name:
 - PRJ_NOTIFICATION
product: Windows
targetos: Windows
req.typenames: PRJ_NOTIFICATION
req.redist: 
---

# PRJ_NOTIFICATION enumeration


## -description


A notification value specified when sending the notification in a callback


## -enum-fields




### -field PRJ_NOTIFICATION_FILE_OPENED

If received in a notification:

<ul>
<li>Indicates that a handle has been created to an existing file or folder.</li>
<li>The provider can specify a new notification mask for this file or folder when responding to the notification.</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>This indicates that the provider should be notified when a handle is created to an existing file or folder.</li>
</ul>
If specified in response to a notification:

<ul>
<li>This indicates that the provider should be notified if any further handles are created to the file or folder.</li>
</ul>

### -field PRJ_NOTIFICATION_NEW_FILE_CREATED

If received in a notification:

<ul>
<li>A new file or folder has been created.</li>
<li>The provider can specify a new notification mask for this file or folder when responding to the notification.</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>The provider should be notified when a new file or folder is created.</li>
</ul>
If specified in response to a notification:

<ul>
<li>No effect.</li>
</ul>

### -field PRJ_NOTIFICATION_FILE_OVERWRITTEN

If received in a notification:

<ul>
<li>An existing file has been overwritten or superceded.</li>
<li>The provider can specify a new notification mask for this file or folder when responding to the notification.</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>Indicates that the provider should be notified when an existing when an existing file is overwritten or superceded.</li>
</ul>
If specified in response to a notification:

<ul>
<li>Indicates that the provider should be notified when the file or folder is overwritten or superceded.</li>
</ul>

### -field PRJ_NOTIFICATION_PRE_DELETE

If received in a notification:

<ul>
<li>A file or folder is about to be deleted.</li>
<li>If the provider returns an error HRESULT code from the callback, the delete will not take effect. </li>
</ul>
If specified on virtualization instance start:

<ul>
<li>Indicates that the provider should be notified when a file or folder is about to be deleted.</li>
</ul>
If specified in response to a notification:

<ul>
<li>Indicates that the provider should be notified when a file or folder is about to be deleted.</li>
</ul>

### -field PRJ_NOTIFICATION_PRE_RENAME

If received in a notification:

<ul>
<li>A file or folder is about to be renamed.</li>
<li>If the provider returns an error HRESULT code from the callback, the rename will not take effect.</li>
<li>If the callbackData-&gt;FilePathName parameter of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> is an empty string, this indicates that the rename is moving the file/directory from outside the virtualization instance. In that case, this notification will always be sent if the provider has registered a <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> callback, even if the provider did not specify this bit when registering the subtree containing the destination path. However if the provider specified PRJ_NOTIFICATION_SUPPRESS_NOTIFICATIONS when registering the subtree containing the destination path, the notification will be suppressed. 
</li>
<li>If the destinationFileName parameter of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> is an empty string, this indicates that the rename is moving the file/folder out of the virtualization instance. 
</li>
<li>If both the callbackData-&gt;FilePathName and destinationFileName parameters of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> are non-empty strings, this indicates that the rename is within the virtualization instance. If the provider specified different notification masks for the source and destination paths in the NotificationMappings member of the options parameter of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing">PrjStartVirtualizing</a>, then this notification will be sent if the provider specified this bit when registering either the source or destination paths. </li>
</ul>
If specified on virtualization instance start:

<ul>
<li>Indicates that the provider should be notified when a file or folder is about to be renamed.</li>
</ul>
If specified in response to a notification:

<ul>
<li>Indicates that the provider should be notified when a file or folder is about to be renamed.</li>
</ul>

### -field PRJ_NOTIFICATION_PRE_SET_HARDLINK

If received in a notification:

<ul>
<li>A hard link is about to be created for the file.</li>
<li>If the provider returns an error HRESULT code from the callback, the hard link operation will not take effect. 
</li>
<li>If the callbackData-&gt;FilePathName parameter of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> is an empty string, this indicates that the hard link name will be created inside the virtualization instance, i.e. a new hard link is being created inside the virtualization instance to a file that exists outside the virtualization instance. In that case, this notification will always be sent if the provider has registered a <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> callback, even if the provider did not specify this bit when registering the subtree where the new hard link name will be. However if the provider specified PRJ_NOTIFICATION_SUPPRESS_NOTIFICATIONS when registering the subtree containing the destination path, the notification will be suppressed.</li>
<li>If the destinationFileName parameter of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> is an empty string, this indicates that the hard link name will be created outside the virtualization instance, i.e. a new hard link is being created outside the virtualization instance for a file that exists inside the virtualization instance. 
</li>
<li>If both the callbackData-&gt;FilePathName and destinationFileName parameters of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> are non-empty strings, this indicates that the new hard link will be created within the virtualization instance for a file that exists within the virtualization instance. If the provider specified different notification masks for the source and destination paths in the NotificationMappings member of the options parameter of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing">PrjStartVirtualizing</a>, then this notification will be sent if the provider specified this bit when registering either the source or destination paths.</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>Indicates that the provider should be notified when a hard link is about to be created for a file.</li>
</ul>
If specified in response to a notification:

<ul>
<li>Indicates that the provider should be notified when a hard link is about to be created for a file.</li>
</ul>

### -field PRJ_NOTIFICATION_FILE_RENAMED

If received in a notification:

<ul>
<li>Indicates that a file/folder has been renamed. The file/folder may have been moved into the virtualization instance.</li>
<li>If the callbackData-&gt;FilePathName parameter of PRJ_NOTIFICATION_CB is an empty string, this indicates that the rename moved the file/directory from outside the virtualization instance. In that case ProjFS will always send this notification if the provider has registered a PRJ_NOTIFICATION_CB 
callback, even if the provider did not specify this bit when registering the subtree containing the destination path. 
</li>
<li>If the destinationFileName parameter of PRJ_NOTIFICATION_CB is an empty string, this indicates that the rename moved the file/directory out of the virtualization instance. 
</li>
<li>If both the callbackData-&gt;FilePathName and destinationFileName parameters of PRJ_NOTIFICATION_CB are non-empty strings, this indicates that the rename was within the virtualization instance. If the provider specified different notification masks for the source and destination paths in the NotificationMappings member of the options parameter of PrjStartVirtualizing, then ProjFS will send this notification if the provider specified this bit when registering either the source or destination paths.</li>
<li>The provider can specify a new notification mask for this file/directory when responding to the notification.</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>Indicates that the provider should be notified that a file or folder has been renamed.</li>
</ul>
If specified in response to a notification:

<ul>
<li>Indicates that the provider should be notified when a file or folder has been renamed.</li>
</ul>

### -field PRJ_NOTIFICATION_HARDLINK_CREATED

If received in a notification:

<ul>
<li>Indicates that a hard link has been created for the file. 
</li>
<li>If the callbackData-&gt;FilePathName parameter of PRJ_NOTIFICATION_CB is an empty string, this indicates that the hard link name was created inside the virtualization instance, i.e. a new hard link was created inside the virtualization instance to a file that exists outside the virtualization instance. In that case ProjFS will always send this notification if the provider has registered a PRJ_NOTIFICATION_CB callback, even if the provider did not specify this bit when registering the subtree where the new hard link name will be. 
</li>
<li>If the destinationFileName parameter of PRJ_NOTIFICATION_CB is an empty string, this indicates that the hard link name was created outside the virtualization instance, i.e. a new hard link was created outside the virtualization instance for a file that exists inside the virtualization instance. 
</li>
<li>If both the callbackData-&gt;FilePathName and destinationFileName parameters of PRJ_NOTIFICATION_CB are non-empty strings, this indicates that the a new hard link was created within the virtualization instance for a file that exists within the virtualization instance. If the provider specified different notification masks for the source and destination paths in the NotificationMappings member of the options parameter of PrjStartVirtualizing, then ProjFS will send this notification if the provider specified this bit when registering either the source or destination paths.</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>Indicates that the provider should be notified that a hard link has been created for a file.</li>
</ul>
If specified in response to a notification:

<ul>
<li>Indicates that the provider should be notified that a hard link has been created for the file.</li>
</ul>

### -field PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION

If received in a notification:

<ul>
<li>A handle has been closed on the file/folder, and the file’s content was not modified while the handle was open, and the file/folder was not deleted</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>The provider should be notified when a handle is closed on a file/folder and the closing handle neither modified nor deleted it.</li>
</ul>
If specified in response to a notification:

<ul>
<li>The provider should be notified when handles are closed for the file/folder and there were no modifications or deletions associated with the closing handle.</li>
</ul>

### -field PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_MODIFIED

If received in a notification:

<ul>
<li>A handle has been closed on the file, and that the file’s content was modified while the handle was open.</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>The provider should be notified when a handle is closed on a file/folder and the closing handle was used to modify it.</li>
</ul>
If specified in response to a notification:

<ul>
<li>The provider should be notified when a handle is closed on the file/folder and the closing handle was used to modify it.</li>
</ul>

### -field PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED

If received in a notification:

<ul>
<li>A handle has been closed on the file/folder, and that it was deleted as part of closing the handle. 
</li>
<li>If the provider also registered to receive PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_MODIFIED notifications, and the file was modified using the handle whose close resulted in deleting the file, then the operationParameters-&gt;FileDeletedOnHandleClose.IsFileModified parameter of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> will be TRUE. This applies only to files, not directories</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>The provider should be notified when a handle is closed on a file/folder and it is deleted as part of closing the handle.</li>
</ul>
If specified in response to a notification:

<ul>
<li>The provider should be notified when a handle is closed on the file/folder and it is deleted as part of closing the handle.</li>
</ul>

### -field PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL




#### - PRJ_NOTIFICATION_PRE_CONVERT_TO_FULL

If received in a notification:

<ul>
<li>The file is about to be expanded from a placeholder to a full file, i.e. its contents are likely to be modified.</li>
<li>If the provider returns an error HRESULT code from the callback, the file will not be expanded to a full file, and the I/O that triggered the conversion will fail.</li>
<li>If there are multiple racing I/Os that would expand the same file, the provider will receive this notification value only once for the file.</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>The provider should be notified when it is about to convert a placeholder to a full file.</li>
</ul>
If specified in response to a notification:

<ul>
<li>The provider should be notified when it is about to convert the placeholder to a full file, assuming it is a placeholder and not already a full file.</li>
</ul>
