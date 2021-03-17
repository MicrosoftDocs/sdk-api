---
UID: NS:projectedfslib.PRJ_NOTIFICATION_PARAMETERS
title: PRJ_NOTIFICATION_PARAMETERS (projectedfslib.h)
description: Extra parameters for notifications.
helpviewer_keywords: ["PRJ_NOTIFICATION_PARAMETERS","PRJ_NOTIFICATION_PARAMETERS union","ProjFS.prj_notification_parameters","projectedfslib/PRJ_NOTIFICATION_PARAMETERS"]
old-location: projfs\prj_notification_parameters.htm
tech.root: ProjFS
ms.assetid: 596DC712-C6DD-4834-9E0F-CA21B0BC3BB3
ms.date: 12/05/2018
ms.keywords: PRJ_NOTIFICATION_PARAMETERS, PRJ_NOTIFICATION_PARAMETERS union, ProjFS.prj_notification_parameters, projectedfslib/PRJ_NOTIFICATION_PARAMETERS
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
req.typenames: PRJ_NOTIFICATION_PARAMETERS
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_NOTIFICATION_PARAMETERS
 - projectedfslib/PRJ_NOTIFICATION_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_NOTIFICATION_PARAMETERS
---

# PRJ_NOTIFICATION_PARAMETERS structure


## -description

Extra parameters for notifications.

## -struct-fields

### -field PostCreate

### -field PostCreate.NotificationMask

Upon return from the <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> callback, the provider may specify a new set of notifications that it wishes to receive for the file here. If the provider sets this value to 0, it is equivalent to specifying <b>PRJ_NOTIFICATION_USE_EXISTING_MASK</b>.

### -field FileRenamed

### -field FileRenamed.NotificationMask

Upon return from the <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> callback, the provider may specify a new set of notifications that it wishes to receive for the file here. If the provider sets this value to 0, it is equivalent to specifying <b>PRJ_NOTIFICATION_USE_EXISTING_MASK</b>.

### -field FileDeletedOnHandleClose

### -field FileDeletedOnHandleClose.IsFileModified

If the provider registered for <b>PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_MODIFIED</b> as well as <b>PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED</b>, this field is set to TRUE if the file was modified before it was deleted.