---
UID: NE:cfapi.CF_CALLBACK_TYPE
title: CF_CALLBACK_TYPE (cfapi.h)
description: Contains the various types of callbacks used on placeholder files or folders.
helpviewer_keywords: ["CF_CALLBACK_TYPE","CF_CALLBACK_TYPE enumeration","CF_CALLBACK_TYPE_CANCEL_FETCH_DATA","CF_CALLBACK_TYPE_CANCEL_FETCH_PLACEHOLDERS","CF_CALLBACK_TYPE_FETCH_DATA","CF_CALLBACK_TYPE_FETCH_PLACEHOLDERS","CF_CALLBACK_TYPE_NONE","CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE","CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE_COMPLETION","CF_CALLBACK_TYPE_NOTIFY_DELETE","CF_CALLBACK_TYPE_NOTIFY_DELETE_COMPLETION","CF_CALLBACK_TYPE_NOTIFY_FILE_CLOSE_COMPLETION","CF_CALLBACK_TYPE_NOTIFY_FILE_OPEN_COMPLETION","CF_CALLBACK_TYPE_NOTIFY_RENAME","CF_CALLBACK_TYPE_NOTIFY_RENAME_COMPLETION","CF_CALLBACK_TYPE_VALIDATE_DATA","cfapi/CF_CALLBACK_TYPE","cfapi/CF_CALLBACK_TYPE_CANCEL_FETCH_DATA","cfapi/CF_CALLBACK_TYPE_CANCEL_FETCH_PLACEHOLDERS","cfapi/CF_CALLBACK_TYPE_FETCH_DATA","cfapi/CF_CALLBACK_TYPE_FETCH_PLACEHOLDERS","cfapi/CF_CALLBACK_TYPE_NONE","cfapi/CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE","cfapi/CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE_COMPLETION","cfapi/CF_CALLBACK_TYPE_NOTIFY_DELETE","cfapi/CF_CALLBACK_TYPE_NOTIFY_DELETE_COMPLETION","cfapi/CF_CALLBACK_TYPE_NOTIFY_FILE_CLOSE_COMPLETION","cfapi/CF_CALLBACK_TYPE_NOTIFY_FILE_OPEN_COMPLETION","cfapi/CF_CALLBACK_TYPE_NOTIFY_RENAME","cfapi/CF_CALLBACK_TYPE_NOTIFY_RENAME_COMPLETION","cfapi/CF_CALLBACK_TYPE_VALIDATE_DATA","cloudApi.cf_callback_type"]
old-location: cloudapi\cf_callback_type.htm
tech.root: cloudapi
ms.assetid: 0BA978D3-110C-47FC-8949-C5D98A59654C
ms.date: 12/05/2018
ms.keywords: CF_CALLBACK_TYPE, CF_CALLBACK_TYPE enumeration, CF_CALLBACK_TYPE_CANCEL_FETCH_DATA, CF_CALLBACK_TYPE_CANCEL_FETCH_PLACEHOLDERS, CF_CALLBACK_TYPE_FETCH_DATA, CF_CALLBACK_TYPE_FETCH_PLACEHOLDERS, CF_CALLBACK_TYPE_NONE, CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE, CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE_COMPLETION, CF_CALLBACK_TYPE_NOTIFY_DELETE, CF_CALLBACK_TYPE_NOTIFY_DELETE_COMPLETION, CF_CALLBACK_TYPE_NOTIFY_FILE_CLOSE_COMPLETION, CF_CALLBACK_TYPE_NOTIFY_FILE_OPEN_COMPLETION, CF_CALLBACK_TYPE_NOTIFY_RENAME, CF_CALLBACK_TYPE_NOTIFY_RENAME_COMPLETION, CF_CALLBACK_TYPE_VALIDATE_DATA, cfapi/CF_CALLBACK_TYPE, cfapi/CF_CALLBACK_TYPE_CANCEL_FETCH_DATA, cfapi/CF_CALLBACK_TYPE_CANCEL_FETCH_PLACEHOLDERS, cfapi/CF_CALLBACK_TYPE_FETCH_DATA, cfapi/CF_CALLBACK_TYPE_FETCH_PLACEHOLDERS, cfapi/CF_CALLBACK_TYPE_NONE, cfapi/CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE, cfapi/CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE_COMPLETION, cfapi/CF_CALLBACK_TYPE_NOTIFY_DELETE, cfapi/CF_CALLBACK_TYPE_NOTIFY_DELETE_COMPLETION, cfapi/CF_CALLBACK_TYPE_NOTIFY_FILE_CLOSE_COMPLETION, cfapi/CF_CALLBACK_TYPE_NOTIFY_FILE_OPEN_COMPLETION, cfapi/CF_CALLBACK_TYPE_NOTIFY_RENAME, cfapi/CF_CALLBACK_TYPE_NOTIFY_RENAME_COMPLETION, cfapi/CF_CALLBACK_TYPE_VALIDATE_DATA, cloudApi.cf_callback_type
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: CF_CALLBACK_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CALLBACK_TYPE
 - cfapi/CF_CALLBACK_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_CALLBACK_TYPE
---

# CF_CALLBACK_TYPE enumeration


## -description

Contains the various types of callbacks used on placeholder files or folders.

## -enum-fields

### -field CF_CALLBACK_TYPE_FETCH_DATA

Callback to satisfy an I/O request, or a placeholder hydration request.

### -field CF_CALLBACK_TYPE_VALIDATE_DATA

Callback to validate placeholder data.

### -field CF_CALLBACK_TYPE_CANCEL_FETCH_DATA

Callback to cancel an ongoing placeholder hydration.

### -field CF_CALLBACK_TYPE_FETCH_PLACEHOLDERS

Callback to request information about the contents of placeholder files.

### -field CF_CALLBACK_TYPE_CANCEL_FETCH_PLACEHOLDERS

Callback to cancel a request for the contents of placeholder files.

### -field CF_CALLBACK_TYPE_NOTIFY_FILE_OPEN_COMPLETION

Callback to inform the sync provider that a placeholder under one of its sync roots has been successfully opened for read/write/delete access.

### -field CF_CALLBACK_TYPE_NOTIFY_FILE_CLOSE_COMPLETION

Callback to inform the sync provider that a placeholder under one of its sync roots that has been previously opened for read/write/delete access is now closed.

### -field CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE

Callback to inform the sync provider that a placeholder under one of its sync roots is about to be dehydrated.

### -field CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE_COMPLETION

Callback to inform the sync provider that a placeholder under one of its sync roots has been successfully dehydrated.

### -field CF_CALLBACK_TYPE_NOTIFY_DELETE

Callback  to inform the sync provider that a placeholder under one of its sync roots is about to be deleted.

### -field CF_CALLBACK_TYPE_NOTIFY_DELETE_COMPLETION

Callback to inform the sync provider that a placeholder under one of its sync roots has been successfully deleted.

### -field CF_CALLBACK_TYPE_NOTIFY_RENAME

Callback to inform the sync provider that a placeholder under one of its sync roots is about to be renamed or moved.

### -field CF_CALLBACK_TYPE_NOTIFY_RENAME_COMPLETION

Callback to inform the sync provider that a placeholder under one of its sync roots has been successfully renamed or moved.

### -field CF_CALLBACK_TYPE_NONE:0xffffffff

No callback type.

## -remarks

These are not APIs provided by the library, but rather callbacks that a sync provider must implement in order to service requests from the platform.  As necessary, the platform will ask the library instance running inside the sync provider process to invoke the appropriate callback routine.


Callback routines will be invoked in an arbitrary thread (part of a thread pool).  Multiple callbacks can occur simultaneously, in different threads, and it is the responsibility of the sync provider code to implement any necessary synchronization to make this work reliably. All callbacks are asynchronous. Asynchronous user requests that trigger the callbacks are pended and the control is returned to the user application.


Every callback request has a fixed 60 second timeout. A valid operation on any pending requests from the sync provider resets the timers of all pending requests.


All callback functions have the same prototype with two arguments: a CF_CALLBACK_INFO structure and a CF_CALLBACK_PARAMETER structure.


Callback routines have no return value.

