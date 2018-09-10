---
UID: NE:cfapi.CF_SYNC_PROVIDER_STATUS
title: CF_SYNC_PROVIDER_STATUS
author: windows-sdk-content
description: Current status of a sync provider.
old-location: cloudapi\cf_sync_provider_status.htm
tech.root: cfApi
ms.assetid: 575A9F66-66D4-4443-9BCB-0CBD60DA27A0
ms.author: windowssdkdev
ms.date: 02/27/2018
ms.keywords: CF_PROVIDER_STATUS_CLEAR_FLAGS, CF_PROVIDER_STATUS_CONNECTIVITY_LOST, CF_PROVIDER_STATUS_DISCONNECTED, CF_PROVIDER_STATUS_IDLE, CF_PROVIDER_STATUS_POPULATE_CONTENT, CF_PROVIDER_STATUS_POPULATE_METADATA, CF_PROVIDER_STATUS_POPULATE_NAMESPACE, CF_PROVIDER_STATUS_SYNC_FULL, CF_PROVIDER_STATUS_SYNC_INCREMENTAL, CF_SYNC_PROVIDER_STATUS, CF_SYNC_PROVIDER_STATUS enumeration, cfapi/CF_PROVIDER_STATUS_CLEAR_FLAGS, cfapi/CF_PROVIDER_STATUS_CONNECTIVITY_LOST, cfapi/CF_PROVIDER_STATUS_DISCONNECTED, cfapi/CF_PROVIDER_STATUS_IDLE, cfapi/CF_PROVIDER_STATUS_POPULATE_CONTENT, cfapi/CF_PROVIDER_STATUS_POPULATE_METADATA, cfapi/CF_PROVIDER_STATUS_POPULATE_NAMESPACE, cfapi/CF_PROVIDER_STATUS_SYNC_FULL, cfapi/CF_PROVIDER_STATUS_SYNC_INCREMENTAL, cfapi/CF_SYNC_PROVIDER_STATUS, cloudApi.cf_sync_provider_status
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_SYNC_PROVIDER_STATUS
product: Windows
targetos: Windows
req.typenames: CF_SYNC_PROVIDER_STATUS
req.redist: 
---

# CF_SYNC_PROVIDER_STATUS enumeration


## -description


Current status of a sync provider.


## -enum-fields




### -field CF_PROVIDER_STATUS_DISCONNECTED

The sync provider is disconnected.


### -field CF_PROVIDER_STATUS_IDLE

The sync provider is idle.


### -field CF_PROVIDER_STATUS_POPULATE_NAMESPACE

The sync provider is populating a namespace.


### -field CF_PROVIDER_STATUS_POPULATE_METADATA

The sync provider is populating placeholder metadata.


### -field CF_PROVIDER_STATUS_POPULATE_CONTENT

The sync provider is populating placeholder content.


### -field CF_PROVIDER_STATUS_SYNC_INCREMENTAL

The sync provider is incrementally syncing placeholder content.


### -field CF_PROVIDER_STATUS_SYNC_FULL

The sync provider has fully synced placeholder file data.


### -field CF_PROVIDER_STATUS_CONNECTIVITY_LOST

The sync provider has lost connectivity.


### -field CF_PROVIDER_STATUS_CLEAR_FLAGS

Clears the flags of the sync provider.


### -field CF_PROVIDER_STATUS_TERMINATED


### -field CF_PROVIDER_STATUS_ERROR



