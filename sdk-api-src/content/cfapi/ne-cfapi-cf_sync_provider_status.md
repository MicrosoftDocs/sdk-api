---
UID: NE:cfapi.CF_SYNC_PROVIDER_STATUS
title: CF_SYNC_PROVIDER_STATUS (cfapi.h)
description: Current status of a sync provider.
helpviewer_keywords: ["CF_PROVIDER_STATUS_CLEAR_FLAGS","CF_PROVIDER_STATUS_CONNECTIVITY_LOST","CF_PROVIDER_STATUS_DISCONNECTED","CF_PROVIDER_STATUS_IDLE","CF_PROVIDER_STATUS_POPULATE_CONTENT","CF_PROVIDER_STATUS_POPULATE_METADATA","CF_PROVIDER_STATUS_POPULATE_NAMESPACE","CF_PROVIDER_STATUS_SYNC_FULL","CF_PROVIDER_STATUS_SYNC_INCREMENTAL","CF_SYNC_PROVIDER_STATUS","CF_SYNC_PROVIDER_STATUS enumeration","cfapi/CF_PROVIDER_STATUS_CLEAR_FLAGS","cfapi/CF_PROVIDER_STATUS_CONNECTIVITY_LOST","cfapi/CF_PROVIDER_STATUS_DISCONNECTED","cfapi/CF_PROVIDER_STATUS_IDLE","cfapi/CF_PROVIDER_STATUS_POPULATE_CONTENT","cfapi/CF_PROVIDER_STATUS_POPULATE_METADATA","cfapi/CF_PROVIDER_STATUS_POPULATE_NAMESPACE","cfapi/CF_PROVIDER_STATUS_SYNC_FULL","cfapi/CF_PROVIDER_STATUS_SYNC_INCREMENTAL","cfapi/CF_SYNC_PROVIDER_STATUS","cloudApi.cf_sync_provider_status"]
old-location: cloudapi\cf_sync_provider_status.htm
tech.root: cloudapi
ms.assetid: 575A9F66-66D4-4443-9BCB-0CBD60DA27A0
ms.date: 12/05/2018
ms.keywords: CF_PROVIDER_STATUS_CLEAR_FLAGS, CF_PROVIDER_STATUS_CONNECTIVITY_LOST, CF_PROVIDER_STATUS_DISCONNECTED, CF_PROVIDER_STATUS_IDLE, CF_PROVIDER_STATUS_POPULATE_CONTENT, CF_PROVIDER_STATUS_POPULATE_METADATA, CF_PROVIDER_STATUS_POPULATE_NAMESPACE, CF_PROVIDER_STATUS_SYNC_FULL, CF_PROVIDER_STATUS_SYNC_INCREMENTAL, CF_SYNC_PROVIDER_STATUS, CF_SYNC_PROVIDER_STATUS enumeration, cfapi/CF_PROVIDER_STATUS_CLEAR_FLAGS, cfapi/CF_PROVIDER_STATUS_CONNECTIVITY_LOST, cfapi/CF_PROVIDER_STATUS_DISCONNECTED, cfapi/CF_PROVIDER_STATUS_IDLE, cfapi/CF_PROVIDER_STATUS_POPULATE_CONTENT, cfapi/CF_PROVIDER_STATUS_POPULATE_METADATA, cfapi/CF_PROVIDER_STATUS_POPULATE_NAMESPACE, cfapi/CF_PROVIDER_STATUS_SYNC_FULL, cfapi/CF_PROVIDER_STATUS_SYNC_INCREMENTAL, cfapi/CF_SYNC_PROVIDER_STATUS, cloudApi.cf_sync_provider_status
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
req.typenames: CF_SYNC_PROVIDER_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_SYNC_PROVIDER_STATUS
 - cfapi/CF_SYNC_PROVIDER_STATUS
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
 - CF_SYNC_PROVIDER_STATUS
---

# CF_SYNC_PROVIDER_STATUS enumeration


## -description

Current status of a sync provider.

## -enum-fields

### -field CF_PROVIDER_STATUS_DISCONNECTED:0x00000000

The sync provider is disconnected.

### -field CF_PROVIDER_STATUS_IDLE:0x00000001

The sync provider is idle.

### -field CF_PROVIDER_STATUS_POPULATE_NAMESPACE:0x00000002

The sync provider is populating a namespace.

### -field CF_PROVIDER_STATUS_POPULATE_METADATA:0x00000004

The sync provider is populating placeholder metadata.

### -field CF_PROVIDER_STATUS_POPULATE_CONTENT:0x00000008

The sync provider is populating placeholder content.

### -field CF_PROVIDER_STATUS_SYNC_INCREMENTAL:0x00000010

The sync provider is incrementally syncing placeholder content.

### -field CF_PROVIDER_STATUS_SYNC_FULL:0x00000020

The sync provider has fully synced placeholder file data.

### -field CF_PROVIDER_STATUS_CONNECTIVITY_LOST:0x00000040

The sync provider has lost connectivity.

### -field CF_PROVIDER_STATUS_CLEAR_FLAGS:0x80000000

Clears the flags of the sync provider.

### -field CF_PROVIDER_STATUS_TERMINATED:0xC0000001

### -field CF_PROVIDER_STATUS_ERROR:0xC0000002

