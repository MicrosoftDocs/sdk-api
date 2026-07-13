---
UID: NS:cfapi.CF_SYNC_ROOT_PROVIDER_INFO
title: CF_SYNC_ROOT_PROVIDER_INFO (cfapi.h)
description: Sync root provider information.
helpviewer_keywords: ["CF_SYNC_ROOT_PROVIDER_INFO","CF_SYNC_ROOT_PROVIDER_INFO structure","cfapi/CF_SYNC_ROOT_PROVIDER_INFO","cloudApi.cf_sync_root_provider_info"]
old-location: cloudapi\cf_sync_root_provider_info.htm
tech.root: cloudapi
ms.assetid: 9EBC64B5-7FB3-41AA-BCB2-29B3E444B463
ms.date: 04/04/2023
ms.keywords: CF_SYNC_ROOT_PROVIDER_INFO, CF_SYNC_ROOT_PROVIDER_INFO structure, cfapi/CF_SYNC_ROOT_PROVIDER_INFO, cloudApi.cf_sync_root_provider_info
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
req.typenames: CF_SYNC_ROOT_PROVIDER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_SYNC_ROOT_PROVIDER_INFO
 - cfapi/CF_SYNC_ROOT_PROVIDER_INFO
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
 - CF_SYNC_ROOT_PROVIDER_INFO
---

## -description

Contains sync root provider information.

## -struct-fields

### -field ProviderStatus

Status of the sync root provider. See [CF_SYNC_PROVIDER_STATUS](ne-cfapi-cf_sync_provider_status.md) for possible values.

### -field ProviderName

Name of the sync root provider. *ProviderName* is an end-user facing string with a maximum length of **CF_MAX_PROVIDER_NAME_LENGTH** (255 characters).

### -field ProviderVersion

Version of the sync root provider. *ProviderVersion* is an end-user facing string with a maximum length of **CF_MAX_PROVIDER_VERSION_LENGTH** (255 characters).

## -see-also

[CfGetSyncRootInfoByPath](nf-cfapi-cfgetsyncrootinfobypath.md)

[CF_SYNC_PROVIDER_STATUS](ne-cfapi-cf_sync_provider_status.md)
