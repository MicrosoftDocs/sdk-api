---
UID: NS:cfapi.CF_PLACEHOLDER_STANDARD_INFO
title: CF_PLACEHOLDER_STANDARD_INFO (cfapi.h)
description: Standard placeholder information.
helpviewer_keywords: ["CF_PLACEHOLDER_STANDARD_INFO","CF_PLACEHOLDER_STANDARD_INFO structure","cfapi/CF_PLACEHOLDER_STANDARD_INFO","cloudApi.cf_placeholder_standard_info"]
old-location: cloudapi\cf_placeholder_standard_info.htm
tech.root: cloudapi
ms.assetid: F0CDC9CD-7D31-4854-9568-8F13516C6D15
ms.date: 04/04/2023
ms.keywords: CF_PLACEHOLDER_STANDARD_INFO, CF_PLACEHOLDER_STANDARD_INFO structure, cfapi/CF_PLACEHOLDER_STANDARD_INFO, cloudApi.cf_placeholder_standard_info
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
req.typenames: CF_PLACEHOLDER_STANDARD_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_PLACEHOLDER_STANDARD_INFO
 - cfapi/CF_PLACEHOLDER_STANDARD_INFO
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
 - CF_PLACEHOLDER_STANDARD_INFO
---

## -description

Standard placeholder information.

## -struct-fields

### -field OnDiskDataSize

Total number of bytes on disk.

### -field ValidatedDataSize

Total number of bytes that are in sync with the cloud.

### -field ModifiedDataSize

Total number of bytes that have been overwritten/appended locally and are not in sync with the cloud.

### -field PropertiesSize

Total number of bytes on disk that are used by all the property blobs.

### -field PinState

The [CF_PIN_STATE](ne-cfapi-cf_pin_state.md) of the placeholder. See [CfSetPinState](nf-cfapi-cfsetpinstate.md) for more details.

### -field InSyncState

The [CF_IN_SYNC_STATE](ne-cfapi-cf_in_sync_state.md) of the placeholder. see [CfSetInSyncState](nf-cfapi-cfsetinsyncstate.md) for more details.

### -field FileId

A 64-bit volume wide non-volatile number that uniquely identifies a file or directory.

### -field SyncRootFileId

The file ID of the sync root directory that contains the file whose placeholder information is to be queried.

### -field FileIdentityLength

Length, in bytes, of the *FileIdentity*.

### -field FileIdentity

An opaque blob supplied by the sync provider to the platform when the placeholder was created. File identity is provided for all sync provider callbacks.

## -see-also

[CF_PIN_STATE](ne-cfapi-cf_pin_state.md)

[CfSetPinState](nf-cfapi-cfsetpinstate.md)

[CF_IN_SYNC_STATE](ne-cfapi-cf_in_sync_state.md)

[CfSetInSyncState](nf-cfapi-cfsetinsyncstate.md)
