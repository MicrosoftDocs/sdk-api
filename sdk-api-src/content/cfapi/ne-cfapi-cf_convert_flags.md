---
UID: NE:cfapi.CF_CONVERT_FLAGS
title: CF_CONVERT_FLAGS (cfapi.h)
description: Normal file/directory to placeholder file/directory conversion flags.
helpviewer_keywords: ["CF_CONVERT_FLAGS","CF_CONVERT_FLAGS enumeration","CF_CONVERT_FLAG_DEHYDRATE","CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION","CF_CONVERT_FLAG_MARK_IN_SYNC","CF_CONVERT_FLAG_NONE","cfapi/CF_CONVERT_FLAGS","cfapi/CF_CONVERT_FLAG_DEHYDRATE","cfapi/CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION","cfapi/CF_CONVERT_FLAG_MARK_IN_SYNC","cfapi/CF_CONVERT_FLAG_NONE","cloudApi.cf_convert_flags"]
old-location: cloudapi\cf_convert_flags.htm
tech.root: cloudapi
ms.assetid: 0342BF0B-509A-4F8D-9557-54E534A3DDFE
ms.date: 03/29/2023
ms.keywords: CF_CONVERT_FLAGS, CF_CONVERT_FLAGS enumeration, CF_CONVERT_FLAG_DEHYDRATE, CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION, CF_CONVERT_FLAG_MARK_IN_SYNC, CF_CONVERT_FLAG_NONE, cfapi/CF_CONVERT_FLAGS, cfapi/CF_CONVERT_FLAG_DEHYDRATE, cfapi/CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION, cfapi/CF_CONVERT_FLAG_MARK_IN_SYNC, cfapi/CF_CONVERT_FLAG_NONE, cloudApi.cf_convert_flags
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
req.typenames: CF_CONVERT_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CONVERT_FLAGS
 - cfapi/CF_CONVERT_FLAGS
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
 - CF_CONVERT_FLAGS
---

# CF_CONVERT_FLAGS enumeration

## -description

Normal file/directory to placeholder file/directory conversion flags.

## -enum-fields

### -field CF_CONVERT_FLAG_NONE:0x00000000

No conversion flags.

### -field CF_CONVERT_FLAG_MARK_IN_SYNC:0x00000001

The platform marks the converted placeholder as in sync with cloud upon a successful conversion of the file.

### -field CF_CONVERT_FLAG_DEHYDRATE:0x00000002

Applicable to files only. When specified, the platform dehydrates the file after converting it to a placeholder successfully. The caller must acquire an exclusive handle when specifying this flag or data corruptions can occur. Note that the platform does not validate the exclusiveness of the handle.

### -field CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION:0x00000004

Applicable for directories only. When specified, it marks the converted placeholder directory as partially populated such that any future access to it will result in a **FETCH_PLACEHOLDERS** callback sent to the sync provider.

### -field CF_CONVERT_FLAG_ALWAYS_FULL:0x00000008

When this flag is present, the newly created placeholder will be marked as always full. Once hydrated, any attempt to dehydrate such a (file) placeholder will fail with error code **ERROR_CLOUD_FILE_DEHYDRATION_DISALLOWED**. This flag is enforced on a placeholder file only. It can be set on a placeholder directory, but it has no effect.

### -field CF_CONVERT_FLAG_FORCE_CONVERT_TO_CLOUD_FILE:0x00000010

When specified, the platform allows a sync engine to atomically convert a non-cloud files placeholder (having another reparse tag/data) to a cloud files placeholder. Note that the API normally fails conversion of any non-placeholder file to a placeholder.

The combination **(CF_CONVERT_FLAG_FORCE_CONVERT_TO_CLOUD_FILE | CF_CONVERT_FLAG_DEHYDRATE)** is especially useful in migration scenarios when certain providers are migrating from another platform to cloud files platform and they intend to convert hydrated placeholders on the older platform to dehydrated placeholders on the cloud files platform atomically. Just this flag should be passed for converting full placeholders to cloud files placeholders. If the older platform implements full files as a regular, non-placeholder files, this flag is not needed. Passing this flag on a directory converts directories to cloud files as well, though the **DEHYDRATE** flag doesn’t apply to directories.

Even when the policy **CF_PLACEHOLDER_MANAGEMENT_POLICY_CONVERT_TO_UNRESTRICTED** was specified with [CfRegisterSyncRoot](nf-cfapi-cfregistersyncroot.md), only processes that have registered/connected to the cloud files sync root are allowed to specify this flag.

>[!NOTE]
>The flag is supported only if the `PlatformVersion.IntegrationNumber` obtained from [CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md) is `0x500` or higher.

## -see-also

[CfConvertToPlaceholder](nf-cfapi-cfconverttoplaceholder.md)

[CfRegisterSyncRoot](nf-cfapi-cfregistersyncroot.md)

[CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md)
