---
UID: NS:cfapi.CF_SYNC_ROOT_STANDARD_INFO
title: CF_SYNC_ROOT_STANDARD_INFO (cfapi.h)
description: Standard sync root information.
helpviewer_keywords: ["CF_SYNC_ROOT_STANDARD_INFO","CF_SYNC_ROOT_STANDARD_INFO structure","cfapi/CF_SYNC_ROOT_STANDARD_INFO","cloudApi.cf_sync_root_standard_info"]
old-location: cloudapi\cf_sync_root_standard_info.htm
tech.root: cloudapi
ms.assetid: 17E409FB-2997-432C-977F-BEBF53068B42
ms.date: 04/04/2023
ms.keywords: CF_SYNC_ROOT_STANDARD_INFO, CF_SYNC_ROOT_STANDARD_INFO structure, cfapi/CF_SYNC_ROOT_STANDARD_INFO, cloudApi.cf_sync_root_standard_info
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
req.typenames: CF_SYNC_ROOT_STANDARD_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_SYNC_ROOT_STANDARD_INFO
 - cfapi/CF_SYNC_ROOT_STANDARD_INFO
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
 - CF_SYNC_ROOT_STANDARD_INFO
---

## -description

Standard sync root information.

## -struct-fields

### -field SyncRootFileId

File ID of the sync root.

### -field HydrationPolicy

Hydration policy of the sync root. See [CF_HYDRATION_POLICY_PRIMARY](ne-cfapi-cf_hydration_policy_primary.md) for more information.

### -field PopulationPolicy

Population policy of the sync root. See [CF_POPULATION_POLICY_PRIMARY](ne-cfapi-cf_population_policy_primary.md) for more information.

### -field InSyncPolicy

In-sync policy of the sync root. See [CF_INSYNC_POLICY](ne-cfapi-cf_insync_policy.md) for possible values.

### -field HardLinkPolicy

Sync root hard linking policy. See [CF_HARDLINK_POLICY](ne-cfapi-cf_hardlink_policy.md) for possible values.

### -field ProviderStatus

Status of the sync root provider. See [CF_SYNC_PROVIDER_STATUS](ne-cfapi-cf_sync_provider_status.md) for possible values.

### -field ProviderName

Name of the sync root. *ProviderName* is an end-user facing string with a maximum length of **CF_MAX_PROVIDER_NAME_LENGTH** (255 characters).

### -field ProviderVersion

Version of the sync root. *ProviderVersion* is an end-user facing string with a maximum length of **CF_MAX_PROVIDER_VERSION_LENGTH** (255 characters).

### -field SyncRootIdentityLength

Length, in bytes, of the *SyncRootIdentity*.

### -field SyncRootIdentity

The identity of the sync root directory.

## -remarks

## -see-also

[CF_HYDRATION_POLICY_PRIMARY](ne-cfapi-cf_hydration_policy_primary.md)

[CF_POPULATION_POLICY_PRIMARY](ne-cfapi-cf_population_policy_primary.md)

[CF_INSYNC_POLICY](ne-cfapi-cf_insync_policy.md)

[CF_HARDLINK_POLICY](ne-cfapi-cf_hardlink_policy.md)

[CF_SYNC_PROVIDER_STATUS](ne-cfapi-cf_sync_provider_status.md)

[CfGetSyncRootInfoByPath](nf-cfapi-cfgetsyncrootinfobypath.md)
