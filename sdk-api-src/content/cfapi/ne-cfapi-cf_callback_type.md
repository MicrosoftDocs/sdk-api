---
UID: NE:cfapi.CF_CALLBACK_TYPE
title: CF_CALLBACK_TYPE (cfapi.h)
description: Contains the various types of callbacks used on placeholder files or folders.
helpviewer_keywords: ["CF_CALLBACK_TYPE","CF_CALLBACK_TYPE enumeration","CF_CALLBACK_TYPE_CANCEL_FETCH_DATA","CF_CALLBACK_TYPE_CANCEL_FETCH_PLACEHOLDERS","CF_CALLBACK_TYPE_FETCH_DATA","CF_CALLBACK_TYPE_FETCH_PLACEHOLDERS","CF_CALLBACK_TYPE_NONE","CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE","CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE_COMPLETION","CF_CALLBACK_TYPE_NOTIFY_DELETE","CF_CALLBACK_TYPE_NOTIFY_DELETE_COMPLETION","CF_CALLBACK_TYPE_NOTIFY_FILE_CLOSE_COMPLETION","CF_CALLBACK_TYPE_NOTIFY_FILE_OPEN_COMPLETION","CF_CALLBACK_TYPE_NOTIFY_RENAME","CF_CALLBACK_TYPE_NOTIFY_RENAME_COMPLETION","CF_CALLBACK_TYPE_VALIDATE_DATA","cfapi/CF_CALLBACK_TYPE","cfapi/CF_CALLBACK_TYPE_CANCEL_FETCH_DATA","cfapi/CF_CALLBACK_TYPE_CANCEL_FETCH_PLACEHOLDERS","cfapi/CF_CALLBACK_TYPE_FETCH_DATA","cfapi/CF_CALLBACK_TYPE_FETCH_PLACEHOLDERS","cfapi/CF_CALLBACK_TYPE_NONE","cfapi/CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE","cfapi/CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE_COMPLETION","cfapi/CF_CALLBACK_TYPE_NOTIFY_DELETE","cfapi/CF_CALLBACK_TYPE_NOTIFY_DELETE_COMPLETION","cfapi/CF_CALLBACK_TYPE_NOTIFY_FILE_CLOSE_COMPLETION","cfapi/CF_CALLBACK_TYPE_NOTIFY_FILE_OPEN_COMPLETION","cfapi/CF_CALLBACK_TYPE_NOTIFY_RENAME","cfapi/CF_CALLBACK_TYPE_NOTIFY_RENAME_COMPLETION","cfapi/CF_CALLBACK_TYPE_VALIDATE_DATA","cloudApi.cf_callback_type"]
old-location: cloudapi\cf_callback_type.htm
tech.root: cloudapi
ms.assetid: 0BA978D3-110C-47FC-8949-C5D98A59654C
ms.date: 08/25/2023
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

This callback is used to ask the sync provider for a range of file data that is required in order to satisfy an I/O request, or an explicit hydration request, on a placeholder. Implementation of this callback is required if the sync provider specifies a hydration policy that is _not_ **ALWAYS_FULL** at the sync root registration time.

### -field CF_CALLBACK_TYPE_VALIDATE_DATA

This callback is used to ask the sync provider for acknowledgement that a given range of file data, which is already present on disk from prior **CF_OPERATION_TYPE_TRANSFER_DATA** operations, is valid and therefore can be used by the platform to satisfy user I/O requests. Implementation of this callback is required only if the sync provider specifies the hydration policy modifier **VALIDATION_REQUIRED** at the sync root registration time.

### -field CF_CALLBACK_TYPE_CANCEL_FETCH_DATA

This callback is used to inform the sync provider that a range of file data is no longer needed, usually because the originating request has been cancelled. This allows the sync provider to stop spending its efforts trying to get the data (cancel outstanding network requests, etc.). Implementation of this callback is optional.

### -field CF_CALLBACK_TYPE_FETCH_PLACEHOLDERS

This callback is used to ask the sync provider to provide information about the contents of a placeholder directory to satisfy a directory query operation or an attempt to open a file underneath the directory. Implementation of this callback is required only if the sync provider specifies a policy other than **CF_POPULATION_POLICY_ALWAYS_FULL** at the sync root registration time.

### -field CF_CALLBACK_TYPE_CANCEL_FETCH_PLACEHOLDERS

This callback is used to inform the sync provider that the contents of a placeholder directory are no longer needed, usually because the originating request has been cancelled. This allows the sync provider to stop spending its efforts trying to get the contents (cancel outstanding network requests, etc.). Implementation of this callback is optional.

### -field CF_CALLBACK_TYPE_NOTIFY_FILE_OPEN_COMPLETION

This callback is used to inform the sync provider that a placeholder under one of its sync roots has been successfully opened for read/write/delete access. The user application that performs the open is not blocked. No response is expected from the sync provider. This notification doesn’t apply to directories. Implementation of this callback is optional.

### -field CF_CALLBACK_TYPE_NOTIFY_FILE_CLOSE_COMPLETION

This callback is used to inform the sync provider that a placeholder under one of its sync roots that has been previously opened for read/write/delete access is now closed. The user application that performs the close is not blocked. No response is expected from the sync provider. This notification doesn’t apply to directories. Implementation of this callback is optional.

### -field CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE

This callback is used to inform the sync provider that a placeholder under one of its sync root is about to be dehydrated. The user application that performs the dehydration is blocked. A response is expected from the sync provider. Implementation of this callback is optional.

### -field CF_CALLBACK_TYPE_NOTIFY_DEHYDRATE_COMPLETION

This callback is used to inform the sync provider that a placeholder under one of its sync roots has been successfully dehydrated. The user application that performs the dehydration is not blocked. No response is expected from the sync provider. Implementation of this callback is optional.

### -field CF_CALLBACK_TYPE_NOTIFY_DELETE

This callback is used to inform the sync provider that a placeholder under one of its sync roots is about to be deleted. The user application that performs the deletion is blocked. A response is expected from the sync provider. Implementation of this callback is optional.

### -field CF_CALLBACK_TYPE_NOTIFY_DELETE_COMPLETION

This callback is used to inform the sync provider that a placeholder under one of its sync roots has been successfully deleted. The user application that performs the deletion is not blocked. No response is expected from the sync provider. Implementation of this callback is optional.

### -field CF_CALLBACK_TYPE_NOTIFY_RENAME

This callback is used to inform the sync provider that a placeholder under one of its sync roots is about to be renamed or moved. The user application that performs the rename/move is blocked. A response is expected from the sync provider. Implementation of this callback is optional.

### -field CF_CALLBACK_TYPE_NOTIFY_RENAME_COMPLETION

This callback is used to inform the sync provider that a placeholder under one of its sync roots has been successfully renamed or moved. The user application that performs the rename/move is not blocked. No response is expected from the sync provider. Implementation of this callback is optional.

### -field CF_CALLBACK_TYPE_NONE:0xffffffff

No callback type.

## -remarks

These are not APIs provided by the library, but rather callbacks that a sync provider must implement in order to service requests from the platform.  As necessary, the platform will ask the library instance running inside the sync provider process to invoke the appropriate callback routine.

Callback routines will be invoked in an arbitrary thread (part of a thread pool).  Multiple callbacks can occur simultaneously, in different threads, and it is the responsibility of the sync provider code to implement any necessary synchronization to make this work reliably. All callbacks are asynchronous. Asynchronous user requests that trigger the callbacks are pended and the control is returned to the user application.

Every callback request has a fixed 60 second timeout. A valid operation on any pending requests from the sync provider resets the timers of all pending requests.

All callback functions have the same prototype with two arguments: a [CF_CALLBACK_INFO](ns-cfapi-cf_callback_info.md) structure and a [CF_CALLBACK_PARAMETERS](ns-cfapi-cf_callback_parameters.md) structure.

Callback routines have no return value.

## -see-also

[CF_CALLBACK_INFO](ns-cfapi-cf_callback_info.md)

[CF_CALLBACK_PARAMETERS](ns-cfapi-cf_callback_parameters.md)
