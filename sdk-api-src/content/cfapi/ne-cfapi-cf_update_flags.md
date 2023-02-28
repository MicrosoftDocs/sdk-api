---
UID: NE:cfapi.CF_UPDATE_FLAGS
title: CF_UPDATE_FLAGS (cfapi.h)
description: Flags for updating a placeholder file or directory.
helpviewer_keywords: ["CF_UPDATE_FLAGS","CF_UPDATE_FLAGS enumeration","CF_UPDATE_FLAG_CLEAR_IN_SYNC","CF_UPDATE_FLAG_DEHYDRATE","CF_UPDATE_FLAG_DISABLE_ON_DEMAND_POPULATION","CF_UPDATE_FLAG_ENABLE_ON_DEMAND_POPULATION","CF_UPDATE_FLAG_MARK_IN_SYNC","CF_UPDATE_FLAG_NONE","CF_UPDATE_FLAG_ALLOW_PARTIAL","CF_UPDATE_FLAG_ALWAYS_FULL","CF_UPDATE_FLAG_PASSTHROUGH_FS_METADATA","CF_UPDATE_FLAG_REMOVE_FILE_IDENTITY","CF_UPDATE_FLAG_REMOVE_PROPERTY","CF_UPDATE_FLAG_VERIFY_IN_SYNC","cfapi/CF_UPDATE_FLAG_ALLOW_PARTIAL","cfapi/CF_UPDATE_FLAG_ALWAYS_FULL","cfapi/CF_UPDATE_FLAG_PASSTHROUGH_FS_METADATA","cfapi/CF_UPDATE_FLAG_REMOVE_PROPERTY","cfapi/CF_UPDATE_FLAGS","cfapi/CF_UPDATE_FLAG_CLEAR_IN_SYNC","cfapi/CF_UPDATE_FLAG_DEHYDRATE","cfapi/CF_UPDATE_FLAG_DISABLE_ON_DEMAND_POPULATION","cfapi/CF_UPDATE_FLAG_ENABLE_ON_DEMAND_POPULATION","cfapi/CF_UPDATE_FLAG_MARK_IN_SYNC","cfapi/CF_UPDATE_FLAG_NONE","cfapi/CF_UPDATE_FLAG_REMOVE_FILE_IDENTITY","cfapi/CF_UPDATE_FLAG_VERIFY_IN_SYNC","cloudApi.cf_update_flags"]
old-location: cloudapi\cf_update_flags.htm
tech.root: cloudapi
ms.assetid: 83EBEF22-9EAE-4B51-AA23-325FA96EB070
ms.date: 02/28/2023
ms.keywords: CF_UPDATE_FLAGS, CF_UPDATE_FLAGS enumeration, CF_UPDATE_FLAG_CLEAR_IN_SYNC, CF_UPDATE_FLAG_DEHYDRATE, CF_UPDATE_FLAG_DISABLE_ON_DEMAND_POPULATION, CF_UPDATE_FLAG_ENABLE_ON_DEMAND_POPULATION, CF_UPDATE_FLAG_MARK_IN_SYNC, CF_UPDATE_FLAG_NONE, CF_UPDATE_FLAG_ALLOW_PARTIAL, CF_UPDATE_FLAG_ALWAYS_FULL, CF_UPDATE_FLAG_PASSTHROUGH_FS_METADATA, CF_UPDATE_FLAG_REMOVE_FILE_IDENTITY, CF_UPDATE_FLAG_REMOVE_PROPERTY, CF_UPDATE_FLAG_VERIFY_IN_SYNC, cfapi/CF_UPDATE_FLAG_ALLOW_PARTIAL, cfapi/CF_UPDATE_FLAG_ALWAYS_FULL, cfapi/ CF_UPDATE_FLAG_PASSTHROUGH_FS_METADATA, cfapi/ CF_UPDATE_FLAG_REMOVE_PROPERTY, cfapi/CF_UPDATE_FLAGS, cfapi/CF_UPDATE_FLAG_CLEAR_IN_SYNC, cfapi/CF_UPDATE_FLAG_DEHYDRATE, cfapi/CF_UPDATE_FLAG_DISABLE_ON_DEMAND_POPULATION, cfapi/CF_UPDATE_FLAG_ENABLE_ON_DEMAND_POPULATION, cfapi/CF_UPDATE_FLAG_MARK_IN_SYNC, cfapi/CF_UPDATE_FLAG_NONE, cfapi/CF_UPDATE_FLAG_REMOVE_FILE_IDENTITY, cfapi/CF_UPDATE_FLAG_VERIFY_IN_SYNC, cloudApi.cf_update_flags
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
req.typenames: CF_UPDATE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_UPDATE_FLAGS
 - cfapi/CF_UPDATE_FLAGS
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
 - CF_UPDATE_FLAGS
---

# CF_UPDATE_FLAGS enumeration

## -description

Flags for updating a placeholder file or directory.

## -enum-fields

### -field CF_UPDATE_FLAG_NONE

`0x00000000`

No update flags.

### -field CF_UPDATE_FLAG_VERIFY_IN_SYNC

`0x00000001`

The update will fail if the **CF_UPDATE_FLAG_MARK_IN_SYNC** attribute is not currently set on the placeholder.  This is to prevent a race between syncing changes from the cloud down to a local placeholder and the placeholder’s data stream getting locally modified.

### -field CF_UPDATE_FLAG_MARK_IN_SYNC

`0x00000002`

The platform marks the placeholder as in-sync upon a successful update placeholder operation.

### -field CF_UPDATE_FLAG_DEHYDRATE

`0x00000004`

Applicable to files only. When specified, the platform dehydrates the file after updating the placeholder successfully. The caller must acquire an exclusive handle when specifying this flag or data corruptions can occur. Note that the platform does not validate the exclusiveness of the handle.

### -field CF_UPDATE_FLAG_ENABLE_ON_DEMAND_POPULATION

`0x00000008`

Applicable to directories only. When specified, it marks the updated placeholder directory partially populated such that any future access to it will result in a FETCH_PLACEHOLDERS callback sent to the sync provider.

### -field CF_UPDATE_FLAG_DISABLE_ON_DEMAND_POPULATION

`0x00000010`

Applicable to directories only. When specified, it marks the updated placeholder directory fully populated such that any future access to it will be handled by the platform without any callbacks to the sync provider.

### -field CF_UPDATE_FLAG_REMOVE_FILE_IDENTITY

`0x00000020`

When specified, _FileIdentity_ and _FileIdentityLength_ in [CfUpdatePlaceholder](/windows/win32/api/cfapi/nf-cfapi-cfupdateplaceholder) are ignored and the platform will remove the existing file identity blob on the placeholder upon a successful update call.

### -field CF_UPDATE_FLAG_CLEAR_IN_SYNC

`0x00000040`

The platform marks the placeholder as not in-sync upon a successful update placeholder operation.

### -field CF_UPDATE_FLAG_REMOVE_PROPERTY

`0x00000080`

The platform removes all existing extrinsic properties on the placeholder.

> [!NOTE]
> This value is available in Windows 10, version 1803 and later.

### -field CF_UPDATE_FLAG_PASSTHROUGH_FS_METADATA

`0x00000100`

The platform passes **CF_FS_METADATA** to the file system without any filtering; otherwise, the platform skips setting any fields whose value is 0.

> [!NOTE]
> This value is available in Windows 10, version 1803 and later.

### -field CF_UPDATE_FLAG_ALWAYS_FULL

`0x00000200`

`CF_UPDATE_FLAG_ALWAYS_FULL` is effective on placeholder files only. When specified, the placeholder to be updated is marked always full. Once hydrated, any attempt to dehydrate such a placeholder file will fail with error code `ERROR_CLOUD_FILE_DEHYDRATION_DISALLOWED`.

### -field CF_UPDATE_FLAG_ALLOW_PARTIAL

`0x00000400`

`CF_UPDATE_FLAG_ALLOW_PARTIAL` is effective on placeholder files only. When specified, the always full state on a placeholder file, if present, is cleared thus allowing it to be dehydrated again. It is invalid to specify this flag along with `CF_UPDATE_FLAG_ALWAYS_FULL` and error code `ERROR_CLOUD_FILE_INVALID_REQUEST` will be returned as a result.

## -see-also

[CfUpdatePlaceholder](/windows/win32/api/cfapi/nf-cfapi-cfupdateplaceholder)
