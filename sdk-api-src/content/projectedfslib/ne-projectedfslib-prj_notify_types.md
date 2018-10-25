---
UID: NE:projectedfslib.PRJ_NOTIFY_TYPES
title: PRJ_NOTIFY_TYPES
author: windows-sdk-content
description: Types of notifications describing a change to the file or folder.
old-location: projfs\prj_notification_types.htm
tech.root: ProjFS
ms.assetid: AB19AD36-44FB-4CA8-9101-4EEF2646A46C
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED, PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_MODIFIED, PRJ_NOTIFY_FILE_HANDLE_CLOSED_NO_MODIFICATION, PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_FILE_OVERWRITTEN, PRJ_NOTIFY_FILE_PRE_CONVERT_TO_FULL, PRJ_NOTIFY_FILE_RENAMED, PRJ_NOTIFY_HARDLINK_CREATED, PRJ_NOTIFY_NEW_FILE_CREATED, PRJ_NOTIFY_NONE, PRJ_NOTIFY_PRE_DELETE, PRJ_NOTIFY_PRE_RENAME, PRJ_NOTIFY_PRE_SET_HARDLINK, PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS, PRJ_NOTIFY_TYPES, PRJ_NOTIFY_TYPES enumeration, PRJ_NOTIFY_USE_EXISTING_MASK, ProjFS.prj_notification_types, projectedfslib/PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED, projectedfslib/PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_MODIFIED, projectedfslib/PRJ_NOTIFY_FILE_HANDLE_CLOSED_NO_MODIFICATION, projectedfslib/PRJ_NOTIFY_FILE_OPENED, projectedfslib/PRJ_NOTIFY_FILE_OVERWRITTEN, projectedfslib/PRJ_NOTIFY_FILE_PRE_CONVERT_TO_FULL, projectedfslib/PRJ_NOTIFY_FILE_RENAMED, projectedfslib/PRJ_NOTIFY_HARDLINK_CREATED, projectedfslib/PRJ_NOTIFY_NEW_FILE_CREATED, projectedfslib/PRJ_NOTIFY_NONE, projectedfslib/PRJ_NOTIFY_PRE_DELETE, projectedfslib/PRJ_NOTIFY_PRE_RENAME, projectedfslib/PRJ_NOTIFY_PRE_SET_HARDLINK, projectedfslib/PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS, projectedfslib/PRJ_NOTIFY_TYPES, projectedfslib/PRJ_NOTIFY_USE_EXISTING_MASK
ms.prod: windows
ms.technology: windows-sdk
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
 - PRJ_NOTIFY_TYPES
product: Windows
targetos: Windows
req.typenames: PRJ_NOTIFY_TYPES
req.redist: 
---

# PRJ_NOTIFY_TYPES enumeration


## -description


Types of notifications describing a change to the file or folder.


## -enum-fields




### -field PRJ_NOTIFY_NONE

No notification.


### -field PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS

If received in a notification:

<ul>
<li>This notification value is not sent.</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>This indicates that notifications should not be sent for the virtualization instance, or a specified subtree of the instance.</li>
</ul>
If specified in response to a notification:

<ul>
<li>This indicates that notifications should not be sent for the specified file or folder until all handles to it are closed.</li>
</ul>
<div class="alert"><b>Note</b>  If this bit appears in a notification mask, it overrides all other bits in the mask. For example, a valid mask with this bit is treated as containing only PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS.</div>
<div> </div>

### -field PRJ_NOTIFY_FILE_OPENED

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

### -field PRJ_NOTIFY_NEW_FILE_CREATED

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

### -field PRJ_NOTIFY_FILE_OVERWRITTEN

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

### -field PRJ_NOTIFY_PRE_DELETE

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

### -field PRJ_NOTIFY_PRE_RENAME

If received in a notification:

<ul>
<li>A file or folder is about to be renamed.</li>
<li>If the provider returns an error HRESULT code from the callback, the rename will not take effect.</li>
<li>If the callbackData-&gt;FilePathName parameter of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> is an empty string, this indicates that the rename is moving the file/directory from outside the virtualization instance. In that case, this notification will always be sent if the provider has registered a <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> callback, even if the provider did not specify this bit when registering the subtree containing the destination path. However if the provider specified PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS when registering the subtree containing the destination path, the notification will be suppressed. 
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

### -field PRJ_NOTIFY_PRE_SET_HARDLINK

If received in a notification:

<ul>
<li>A hard link is about to be created for the file.</li>
<li>If the provider returns an error HRESULT code from the callback, the hard link operation will not take effect. 
</li>
<li>If the callbackData-&gt;FilePathName parameter of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> is an empty string, this indicates that the hard link name will be created inside the virtualization instance, i.e. a new hard link is being created inside the virtualization instance to a file that exists outside the virtualization instance. In that case, this notification will always be sent if the provider has registered a <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> callback, even if the provider did not specify this bit when registering the subtree where the new hard link name will be. However if the provider specified PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS when registering the subtree containing the destination path, the notification will be suppressed.</li>
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

### -field PRJ_NOTIFY_FILE_RENAMED

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

### -field PRJ_NOTIFY_HARDLINK_CREATED

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

### -field PRJ_NOTIFY_FILE_HANDLE_CLOSED_NO_MODIFICATION

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

### -field PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_MODIFIED

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

### -field PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED

If received in a notification:

<ul>
<li>A handle has been closed on the file/folder, and that it was deleted as part of closing the handle. 
</li>
<li>If the provider also registered to receive PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_MODIFIED notifications, and the file was modified using the handle whose close resulted in deleting the file, then the operationParameters-&gt;FileDeletedOnHandleClose.IsFileModified parameter of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> will be TRUE. This applies only to files, not directories</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>The provider should be notified when a handle is closed on a file/folder and it is deleted as part of closing the handle.</li>
</ul>
If specified in response to a notification:

<ul>
<li>The provider should be notified when a handle is closed on the file/folder and it is deleted as part of closing the handle.</li>
</ul>

### -field PRJ_NOTIFY_FILE_PRE_CONVERT_TO_FULL

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

### -field PRJ_NOTIFY_USE_EXISTING_MASK

If received in a notification:

<ul>
<li>This notification is not sent by the API.</li>
</ul>
If specified on virtualization instance start:

<ul>
<li>This value is not valid on virtualization instance start.</li>
</ul>
If specified in response to a notification:

<ul>
<li> Continue to use the existing set of notifications for this file/folder.</li>
</ul>

## -remarks



ProjFS can send notifications of file system activity to a provider. When the provider starts a virtualization instance it specifies which notifications it wishes to receive. It may also specify a new set of notifications for a file when it is created or renamed. The provider must register a PRJ_NOTIFICATION_CB notification callback routine in the callbacks parameter of PrjStartVirtualizing in order to receive notifications. 


ProjFS sends notifications for files and directories within an active virtualization root. That is, ProjFS will send notifications for the virtualization root and its descendants. Symbolic links and junctions within the virtualization root are not traversed when determining what constitutes a descendant of the virtualization root. 


ProjFS sends notifications only for the primary data stream of a file. ProjFS does not send notifications for operations on alternate data streams. 



ProjFS does not send notifications for an inactive virtualization instance. A virtualization instance is inactive if any one of the following is true: 

<ul>
<li>The provider has not yet started it by calling <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing">PrjStartVirtualizing</a>.</li>
<li>The provider has stopped the instance by calling <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing">PrjStopVirtualizing</a>.</li>
<li>The provider process has exited</li>
</ul> 
The provider may specify which notifications it wishes to receive when starting a virtualization instance, or in response to a notification that allows a new notification mask to be set. 


The provider specifies a default set of notifications that it wants ProjFS to send for the virtualization instance when it starts the instance. This set of notifications is provided in the NotificationMappings member of the options parameter of <a href="https://docs.microsoft.com/en-us/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing">PrjStartVirtualizing</a>, which may specify different notification masks for different subtrees of the virtualization instance. 


The provider may choose to supply a different notification mask in response to a notification of file open, create, supersede/overwrite, or rename. ProjFS will continue to send these notifications for the given file until all handles to the file are closed. After that it will revert to the default set of notifications. Naturally if the default set of notifications does not specify that ProjFS should notify for open, create, etc., the provider will not get the opportunity to specify a different mask for those operations.



