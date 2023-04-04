---
UID: NF:cfapi.CfUnregisterSyncRoot
title: CfUnregisterSyncRoot function (cfapi.h)
description: Unregisters a previously registered sync root.
helpviewer_keywords: ["CfUnregisterSyncRoot","CfUnregisterSyncRoot function","cfapi/CfUnregisterSyncRoot","cloudApi.cfunregistersyncroot"]
old-location: cloudapi\cfunregistersyncroot.htm
tech.root: cloudapi
ms.assetid: B4DA85DB-A63A-45EB-9F71-9395AC026A0C
ms.date: 03/31/2023
ms.keywords: CfUnregisterSyncRoot, CfUnregisterSyncRoot function, cfapi/CfUnregisterSyncRoot, cloudApi.cfunregistersyncroot
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
 - CfUnregisterSyncRoot
 - cfapi/CfUnregisterSyncRoot
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
 - CfUnregisterSyncRoot
---

# CfUnregisterSyncRoot function

## -description

Unregisters a previously registered sync root.

## -parameters

### -param SyncRootPath [in]

The path to the sync root to be unregistered.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

Unregisters a sync root that was registered with [CfRegisterSyncRoot](nf-cfapi-cfregistersyncroot.md). This is typically called at the sync provider uninstall time, when a user account is deleted, or when a user opts to no longer sync a directory tree (if supported by the sync provider). If the sync root to be unregistered has never been registered before, the API fails with **STATUS_CLOUD_FILE_NOT_UNDER_SYNC_ROOT**.

The sync provider should have **WRITE_DATA** or **WRITE_DAC** access to the sync root to be unregistered, or  unregistration will fail with **HRESULT(ERROR_CLOUD_FILE_ACCESS_DENIED)**. Unregistration will also fail with **HRESULT(ERROR_CLOUD_FILE_INVALID_REQUEST)** if a sync provider is *connected* to the sync root.

Unregisters a sync root by traversing the directory tree of the sync root.

For placeholder files:

- If a placeholder file is fully hydrated, it is reverted back to a "normal" file.
- If a placeholder file is not hydrated, it is permanently deleted from the local machine.

For placeholder directories:

- If a placeholder directory is fully populated, it is reverted back to a "normal" directory.
- If a placeholder directory is not fully populated, the directory is permanently deleted from the local machine.

>[!NOTE]
>If the placeholder files or directories cannot be reverted or deleted, it will be skipped, and the unregistering process will continue until the full sync root tree has been traversed.

## -see-also

[CfRegisterSyncRoot](nf-cfapi-cfregistersyncroot.md)
