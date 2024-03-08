---
UID: NF:cfapi.CfQuerySyncProviderStatus
title: CfQuerySyncProviderStatus function (cfapi.h)
description: Queries a sync provider to get the status of the provider.
helpviewer_keywords: ["CfQuerySyncProviderStatus","CfQuerySyncProviderStatus function","cfapi/CfQuerySyncProviderStatus","cloudApi.cfquerysyncproviderstatus"]
old-location: cloudapi\cfquerysyncproviderstatus.htm
tech.root: cloudapi
ms.assetid: 02E6197B-D84A-4E3F-A74C-F5DACAA60AF9
ms.date: 03/30/2023
ms.keywords: CfQuerySyncProviderStatus, CfQuerySyncProviderStatus function, cfapi/CfQuerySyncProviderStatus, cloudApi.cfquerysyncproviderstatus
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
 - CfQuerySyncProviderStatus
 - cfapi/CfQuerySyncProviderStatus
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
 - CfQuerySyncProviderStatus
---

# CfQuerySyncProviderStatus function

## -description

Queries a sync provider to get the status of the provider.

## -parameters

### -param ConnectionKey [in]

A connection key representing a communication channel with the sync filter.

### -param ProviderStatus [out]

The current status of the sync provider.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -see-also

[CF_SYNC_PROVIDER_STATUS](ne-cfapi-cf_sync_provider_status.md)
