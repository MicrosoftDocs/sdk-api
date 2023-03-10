---
UID: NS:syncregistration._SyncProviderConfiguration
title: SyncProviderConfiguration (syncregistration.h)
description: Represents the information for a synchronization provider configuration.
helpviewer_keywords: ["SyncProviderConfiguration","SyncProviderConfiguration structure [Windows Sync]","syncregistration/SyncProviderConfiguration","winsync.syncproviderconfiguration"]
old-location: winsync\syncproviderconfiguration.htm
tech.root: winsync
ms.assetid: 2b8c9a94-4e11-4904-a6aa-da0433d5b237
ms.date: 12/05/2018
ms.keywords: SyncProviderConfiguration, SyncProviderConfiguration structure [Windows Sync], syncregistration/SyncProviderConfiguration, winsync.syncproviderconfiguration
req.header: syncregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SyncProviderConfiguration
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SyncProviderConfiguration
 - syncregistration/_SyncProviderConfiguration
 - SyncProviderConfiguration
 - syncregistration/SyncProviderConfiguration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Syncregistration.h
api_name:
 - SyncProviderConfiguration
---

# SyncProviderConfiguration structure


## -description

Represents the information for a synchronization provider configuration. This structure is passed to the [ISyncProviderRegistration::CreateSyncProviderRegistrationInstance](./nf-syncregistration-isyncproviderregistration-createsyncproviderregistrationinstance.md) method when a registration instance is created.

## -struct-fields

### -field dwVersion

The version of the synchronization provider. The constant value <b>SYNC_PROVIDER_CONFIGURATION_VERSION.</b>

### -field guidInstanceId

The unique instance ID of the synchronization provider.

### -field clsidProvider

The COM CLSID of the synchronization provider.

### -field guidConfigUIInstanceId

The instance ID of the configuration UI used to create this synchronization provider, or <b>GUID_NULL</b> if no configuration UI was used.

### -field guidContentType

The GUID that identifies the content type.

### -field dwCapabilities

One of the following constants that represent the capabilities of the synchronization provider.

<ul>
<li><b>SPC_DEFAULT</b> ((DWORD)0x00000000)</li>
</ul>

### -field dwSupportedArchitecture

One of the following constants that represent the architectures supported by the synchronization provider. This value corresponds to the architectures that the synchronization provider CLSID (<b>clsidProvider</b>) is registered for.   These values can be combined, and can be used as bitmasks.

<ul>
<li><b>SYNC_32_BIT_SUPPORTED</b> ((DWORD)0x00000001)</li>
<li><b>SYNC_64_BIT_SUPPORTED</b> ((DWORD)0x00000002)</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-registration-structures">Windows Sync Registration Structures</a>