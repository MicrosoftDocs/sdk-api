---
UID: NF:cfapi.CfSetInSyncState
title: CfSetInSyncState function (cfapi.h)
description: Sets the in-sync state for a placeholder file or folder.
helpviewer_keywords: ["CfSetInSyncState","CfSetInSyncState function","cfapi/CfSetInSyncState","cloudApi.cfsetinsyncstate"]
old-location: cloudapi\cfsetinsyncstate.htm
tech.root: cloudapi
ms.assetid: 1CB7955D-E530-4F34-8D67-BC608F8B6AF1
ms.date: 03/31/2023
ms.keywords: CfSetInSyncState, CfSetInSyncState function, cfapi/CfSetInSyncState, cloudApi.cfsetinsyncstate
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
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfSetInSyncState
 - cfapi/CfSetInSyncState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfSetInSyncState
---

# CfSetInSyncState function

## -description

Sets the in-sync state for a placeholder file or folder.

## -parameters

### -param FileHandle [in]

A handle to the placeholder. The platform properly synchronizes the operation with other active requests. An attribute or no-access handle is sufficient. The caller must have **WRITE_DATA** or **WRITE_DAC** access to the placeholder.

### -param InSyncState [in]

The in-sync state. *InSyncState* can be set to one of the following values:

- If **CF_IN_SYNC_STATE_NOT_IN_SYNC** is specified, the platform clears the placeholder’s in-sync state upon a successful return from the API call.
- If **CF_IN_SYNC_STATE_IN_SYNC** is specified, the platform sets the placeholder’s in-sync state upon a successful return from the API call.

### -param InSyncFlags [in]

The in-sync state flags. See [CF_SET_IN_SYNC_FLAGS](ne-cfapi-cf_set_in_sync_flags.md) for more details.

### -param InSyncUsn [in, out, optional]

When specified, on input, *InSyncUsn* instructs the platform to only perform in-sync setting if the file still has the same USN value as the one passed in. This is to close a race where the sync provider has just sync’d placeholder changes up to the cloud, but before the call to **CfSetInSyncState**, the placeholder changed in some way. Passing a pointer to a USN value of `0` on input is the same as passing a `NULL` pointer. On return, *InSYncUsn* receives the final USN value after setting the in-sync state.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -see-also

[CF_IN_SYNC_STATE](ne-cfapi-cf_in_sync_state.md)

[CF_SET_IN_SYNC_FLAGS](ne-cfapi-cf_set_in_sync_flags.md)
