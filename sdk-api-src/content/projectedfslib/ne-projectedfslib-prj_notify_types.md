---
UID: NE:projectedfslib.PRJ_NOTIFY_TYPES
title: PRJ_NOTIFY_TYPES (projectedfslib.h)
description: Types of notifications describing a change to the file or folder.
helpviewer_keywords: ["PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED","PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_MODIFIED","PRJ_NOTIFY_FILE_HANDLE_CLOSED_NO_MODIFICATION","PRJ_NOTIFY_FILE_OPENED","PRJ_NOTIFY_FILE_OVERWRITTEN","PRJ_NOTIFY_FILE_PRE_CONVERT_TO_FULL","PRJ_NOTIFY_FILE_RENAMED","PRJ_NOTIFY_HARDLINK_CREATED","PRJ_NOTIFY_NEW_FILE_CREATED","PRJ_NOTIFY_NONE","PRJ_NOTIFY_PRE_DELETE","PRJ_NOTIFY_PRE_RENAME","PRJ_NOTIFY_PRE_SET_HARDLINK","PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS","PRJ_NOTIFY_TYPES","PRJ_NOTIFY_TYPES enumeration","PRJ_NOTIFY_USE_EXISTING_MASK","ProjFS.prj_notification_types","projectedfslib/PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED","projectedfslib/PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_MODIFIED","projectedfslib/PRJ_NOTIFY_FILE_HANDLE_CLOSED_NO_MODIFICATION","projectedfslib/PRJ_NOTIFY_FILE_OPENED","projectedfslib/PRJ_NOTIFY_FILE_OVERWRITTEN","projectedfslib/PRJ_NOTIFY_FILE_PRE_CONVERT_TO_FULL","projectedfslib/PRJ_NOTIFY_FILE_RENAMED","projectedfslib/PRJ_NOTIFY_HARDLINK_CREATED","projectedfslib/PRJ_NOTIFY_NEW_FILE_CREATED","projectedfslib/PRJ_NOTIFY_NONE","projectedfslib/PRJ_NOTIFY_PRE_DELETE","projectedfslib/PRJ_NOTIFY_PRE_RENAME","projectedfslib/PRJ_NOTIFY_PRE_SET_HARDLINK","projectedfslib/PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS","projectedfslib/PRJ_NOTIFY_TYPES","projectedfslib/PRJ_NOTIFY_USE_EXISTING_MASK"]
old-location: projfs\prj_notification_types.htm
tech.root: ProjFS
ms.assetid: AB19AD36-44FB-4CA8-9101-4EEF2646A46C
ms.date: 12/05/2018
ms.keywords: PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED, PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_MODIFIED, PRJ_NOTIFY_FILE_HANDLE_CLOSED_NO_MODIFICATION, PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_FILE_OVERWRITTEN, PRJ_NOTIFY_FILE_PRE_CONVERT_TO_FULL, PRJ_NOTIFY_FILE_RENAMED, PRJ_NOTIFY_HARDLINK_CREATED, PRJ_NOTIFY_NEW_FILE_CREATED, PRJ_NOTIFY_NONE, PRJ_NOTIFY_PRE_DELETE, PRJ_NOTIFY_PRE_RENAME, PRJ_NOTIFY_PRE_SET_HARDLINK, PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS, PRJ_NOTIFY_TYPES, PRJ_NOTIFY_TYPES enumeration, PRJ_NOTIFY_USE_EXISTING_MASK, ProjFS.prj_notification_types, projectedfslib/PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED, projectedfslib/PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_MODIFIED, projectedfslib/PRJ_NOTIFY_FILE_HANDLE_CLOSED_NO_MODIFICATION, projectedfslib/PRJ_NOTIFY_FILE_OPENED, projectedfslib/PRJ_NOTIFY_FILE_OVERWRITTEN, projectedfslib/PRJ_NOTIFY_FILE_PRE_CONVERT_TO_FULL, projectedfslib/PRJ_NOTIFY_FILE_RENAMED, projectedfslib/PRJ_NOTIFY_HARDLINK_CREATED, projectedfslib/PRJ_NOTIFY_NEW_FILE_CREATED, projectedfslib/PRJ_NOTIFY_NONE, projectedfslib/PRJ_NOTIFY_PRE_DELETE, projectedfslib/PRJ_NOTIFY_PRE_RENAME, projectedfslib/PRJ_NOTIFY_PRE_SET_HARDLINK, projectedfslib/PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS, projectedfslib/PRJ_NOTIFY_TYPES, projectedfslib/PRJ_NOTIFY_USE_EXISTING_MASK
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
targetos: Windows
req.typenames: PRJ_NOTIFY_TYPES
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_NOTIFY_TYPES
 - projectedfslib/PRJ_NOTIFY_TYPES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ProjectedFSLib.h
api_name:
 - PRJ_NOTIFY_TYPES
---

# PRJ_NOTIFY_TYPES enumeration


## -description

Types of notifications describing a change to the file or folder.

## -enum-fields

### -field PRJ_NOTIFY_NONE:0x00000000

No notification.

### -field PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS:0x00000001

If specified on virtualization instance start:

- This indicates that notifications should not be sent for the virtualization instance, or a specified subtree of the instance.

If specified in response to a notification:

- This indicates that notifications should not be sent for the specified file or folder until all handles to it are closed.

<div class="alert"><b>Note</b>  If this bit appears in a notification mask, it overrides all other bits in the mask. For example, a valid mask with this bit is treated as containing only PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS.</div>
<div> </div>

### -field PRJ_NOTIFY_FILE_OPENED:0x00000002

If specified on virtualization instance start:

- This indicates that the provider should be notified when a handle is created to an existing file or folder.

If specified in response to a notification:

- This indicates that the provider should be notified if any further handles are created to the file or folder.

### -field PRJ_NOTIFY_NEW_FILE_CREATED:0x00000004

If specified on virtualization instance start:

- The provider should be notified when a new file or folder is created.

If specified in response to a notification:

- No effect.

### -field PRJ_NOTIFY_FILE_OVERWRITTEN:0x00000008

If specified on virtualization instance start:

- Indicates that the provider should be notified when an existing when an existing file is overwritten or superceded.

If specified in response to a notification:

- Indicates that the provider should be notified when the file or folder is overwritten or superceded.

### -field PRJ_NOTIFY_PRE_DELETE:0x00000010

If specified on virtualization instance start:

- Indicates that the provider should be notified when a file or folder is about to be deleted.

If specified in response to a notification:

- Indicates that the provider should be notified when a file or folder is about to be deleted.

### -field PRJ_NOTIFY_PRE_RENAME:0x00000020

If specified on virtualization instance start:

- Indicates that the provider should be notified when a file or folder is about to be renamed.

If specified in response to a notification:

- Indicates that the provider should be notified when a file or folder is about to be renamed.

### -field PRJ_NOTIFY_PRE_SET_HARDLINK:0x00000040

If specified on virtualization instance start:

- Indicates that the provider should be notified when a hard link is about to be created for a file.

If specified in response to a notification:

- Indicates that the provider should be notified when a hard link is about to be created for a file.

### -field PRJ_NOTIFY_FILE_RENAMED:0x00000080

If specified on virtualization instance start:

- Indicates that the provider should be notified that a file or folder has been renamed.

If specified in response to a notification:

- Indicates that the provider should be notified when a file or folder has been renamed.

### -field PRJ_NOTIFY_HARDLINK_CREATED:0x00000100

If specified on virtualization instance start:

- Indicates that the provider should be notified that a hard link has been created for a file.

If specified in response to a notification:

- Indicates that the provider should be notified that a hard link has been created for the file.

### -field PRJ_NOTIFY_FILE_HANDLE_CLOSED_NO_MODIFICATION:0x00000200

If specified on virtualization instance start:

- The provider should be notified when a handle is closed on a file/folder and the closing handle neither modified nor deleted it.

If specified in response to a notification:

- The provider should be notified when handles are closed for the file/folder and there were no modifications or deletions associated with the closing handle.

### -field PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_MODIFIED:0x00000400

If specified on virtualization instance start:

- The provider should be notified when a handle is closed on a file/folder and the closing handle was used to modify it.

If specified in response to a notification:

- The provider should be notified when a handle is closed on the file/folder and the closing handle was used to modify it.

### -field PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED:0x00000800

If specified on virtualization instance start:

- The provider should be notified when a handle is closed on a file/folder and it is deleted as part of closing the handle.

If specified in response to a notification:

- The provider should be notified when a handle is closed on the file/folder and it is deleted as part of closing the handle.

### -field PRJ_NOTIFY_FILE_PRE_CONVERT_TO_FULL:0x00001000

If specified on virtualization instance start:

- The provider should be notified when it is about to convert a placeholder to a full file.

If specified in response to a notification:

- The provider should be notified when it is about to convert the placeholder to a full file, assuming it is a placeholder and not already a full file.

### -field PRJ_NOTIFY_USE_EXISTING_MASK:0xFFFFFFFF

If specified on virtualization instance start:

- This value is not valid on virtualization instance start.

If specified in response to a notification:

-  Continue to use the existing set of notifications for this file/folder.

## -remarks

ProjFS can send notifications of file system activity to a provider. When the provider starts a virtualization instance it specifies which notifications it wishes to receive. It may also specify a new set of notifications for a file when it is created or renamed. The provider must register a PRJ_NOTIFICATION_CB notification callback routine in the callbacks parameter of PrjStartVirtualizing in order to receive notifications. 

ProjFS sends notifications for files and directories within an active virtualization root. That is, ProjFS will send notifications for the virtualization root and its descendants. Symbolic links and junctions within the virtualization root are not traversed when determining what constitutes a descendant of the virtualization root. 

ProjFS sends notifications only for the primary data stream of a file. ProjFS does not send notifications for operations on alternate data streams. 

ProjFS does not send notifications for an inactive virtualization instance. A virtualization instance is inactive if any one of the following is true: 

- The provider has not yet started it by calling <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing">PrjStartVirtualizing</a>.
- The provider has stopped the instance by calling <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing">PrjStopVirtualizing</a>.
- The provider process has exited
 
The provider may specify which notifications it wishes to receive when starting a virtualization instance, or in response to a notification that allows a new notification mask to be set. 

The provider specifies a default set of notifications that it wants ProjFS to send for the virtualization instance when it starts the instance. This set of notifications is provided in the NotificationMappings member of the options parameter of <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing">PrjStartVirtualizing</a>, which may specify different notification masks for different subtrees of the virtualization instance. 

The provider may choose to supply a different notification mask in response to a notification of file open, create, supersede/overwrite, or rename. ProjFS will continue to send these notifications for the given file until all handles to the file are closed. After that it will revert to the default set of notifications. Naturally if the default set of notifications does not specify that ProjFS should notify for open, create, etc., the provider will not get the opportunity to specify a different mask for those operations.
