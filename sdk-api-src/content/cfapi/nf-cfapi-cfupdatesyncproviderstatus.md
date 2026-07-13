---
UID: NF:cfapi.CfUpdateSyncProviderStatus
title: CfUpdateSyncProviderStatus function (cfapi.h)
description: Updates the current status of the sync provider.
helpviewer_keywords: ["CfUpdateSyncProviderStatus","CfUpdateSyncProviderStatus function","cfapi/CfUpdateSyncProviderStatus","cloudApi.cfupdatesyncproviderstatus"]
old-location: cloudapi\cfupdatesyncproviderstatus.htm
tech.root: cloudapi
ms.assetid: E0CB6CA2-439A-4919-95EF-B519ABBBB085
ms.date: 03/31/2023
ms.keywords: CfUpdateSyncProviderStatus, CfUpdateSyncProviderStatus function, cfapi/CfUpdateSyncProviderStatus, cloudApi.cfupdatesyncproviderstatus
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
 - CfUpdateSyncProviderStatus
 - cfapi/CfUpdateSyncProviderStatus
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
 - CfUpdateSyncProviderStatus
---

# CfUpdateSyncProviderStatus function

## -description

Updates the current status of the sync provider.

## -parameters

### -param ConnectionKey [in]

A connection key representing a communication channel with the sync filter.

### -param ProviderStatus [in]

The current status of the sync provider. The status persists for the life of the sync root connection. The sync root connection is torn down either when [CfDisconnectSyncRoot](nf-cfapi-cfdisconnectsyncroot.md) is called or if the sync provider process is terminated.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -see-also

[CfDisconnectSyncRoot](nf-cfapi-cfdisconnectsyncroot.md)

[CF_SYNC_PROVIDER_STATUS](ne-cfapi-cf_sync_provider_status.md)
