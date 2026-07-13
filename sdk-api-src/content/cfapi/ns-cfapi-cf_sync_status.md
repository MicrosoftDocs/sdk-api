---
UID: NS:cfapi.CF_SYNC_STATUS
title: CF_SYNC_STATUS (cfapi.h)
description: Used in a CF_OPERATION_INFO structure to describe the status of a specified sync root.
helpviewer_keywords: ["CF_SYNC_STATUS","CF_SYNC_STATUS structure","PCF_SYNC_STATUS","PCF_SYNC_STATUS structure pointer","cfapi/CF_SYNC_STATUS","cfapi/PCF_SYNC_STATUS","cloudApi.cf_sync_status"]
old-location: cloudapi\cf_sync_status.htm
tech.root: cloudapi
ms.assetid: F80CBBAE-605B-4C1E-BDA5-A4B155F9D079
ms.date: 04/04/2023
ms.keywords: CF_SYNC_STATUS, CF_SYNC_STATUS structure, PCF_SYNC_STATUS, PCF_SYNC_STATUS structure pointer, cfapi/CF_SYNC_STATUS, cfapi/PCF_SYNC_STATUS, cloudApi.cf_sync_status
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
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
req.typenames: CF_SYNC_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_SYNC_STATUS
 - cfapi/CF_SYNC_STATUS
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
 - CF_SYNC_STATUS
---

# CF_SYNC_STATUS structure

## -description

Used in a [CF_OPERATION_INFO](ns-cfapi-cf_operation_info.md) structure to describe the status of a specified sync root.

## -struct-fields

### -field StructSize

The size, in bytes, of the sync status structure, including the actual description string.

### -field Code

The use of this parameter is completely up to the sync provider that supports this rich sync status construct.

For a particular sync provider, it is expected that there is a 1:1 mapping between the code and the description string.

It is recommended that you use the highest bit order to describe the type of error code: `1` for an error-level code, and `0` for an information-level code.

>[!NOTE]
>*Code* is opaque to the platform, and is used only for tracking purposes.

### -field DescriptionOffset

The offset of the description string relative to the start of **CF_SYNC_STATUS**. It points to a localized null-terminated wide string that is expected to contain more meaningful and actionable information about the file in question. Sync providers are expected to balance the requirement of providing more actionable information and maintaining an as small as possible memory footprint.

### -field DescriptionLength

The size of the description string, in bytes, that includes the null terminator.

### -field DeviceIdOffset

The offset of a device id blob relative to the start of **CF_SYNC_STATUS**. The device id blob is optional and opaque to the platform. The blob is expected to be unique on a per device basis. If provided, the blob will be collected as part of the platform telemetry to help diagnose technical issues.

### -field DeviceIdLength

The size of the device id blob, in bytes.

## -remarks

If a null pointer is set in the *SyncStatus* field of a [CF_OPERATION_INFO](ns-cfapi-cf_operation_info.md) structure, the platform will clear the previously set sync status, if there is one.

## -see-also

[CF_OPERATION_INFO](ns-cfapi-cf_operation_info.md)
