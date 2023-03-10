---
UID: NS:cfapi.CF_SYNC_ROOT_STANDARD_INFO
title: CF_SYNC_ROOT_STANDARD_INFO (cfapi.h)
description: Standard sync root information.
helpviewer_keywords: ["CF_SYNC_ROOT_STANDARD_INFO","CF_SYNC_ROOT_STANDARD_INFO structure","cfapi/CF_SYNC_ROOT_STANDARD_INFO","cloudApi.cf_sync_root_standard_info"]
old-location: cloudapi\cf_sync_root_standard_info.htm
tech.root: cloudapi
ms.assetid: 17E409FB-2997-432C-977F-BEBF53068B42
ms.date: 12/05/2018
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

Hydration policy of the sync root.

### -field PopulationPolicy

Population policy of the sync root.

### -field InSyncPolicy

In-sync policy of the sync root.

### -field HardLinkPolicy

Sync root hard linking policy.

### -field ProviderStatus

Status of the sync root provider.

### -field ProviderName

Name of the sync root.

### -field ProviderVersion

Version of the sync root.

### -field SyncRootIdentityLength

Length, in bytes, of the <i>SyncRootIdentity</i>.

### -field SyncRootIdentity

The identity of the sync root directory.

## -remarks

<b>CF_MAX_PROVIDER_NAME_LENGTH</b> and <b>CF_MAX_PROVIDER_VERSION_LENGTH</b>  are set to 255.

