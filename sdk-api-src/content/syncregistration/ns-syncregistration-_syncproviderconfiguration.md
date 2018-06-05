---
UID: NS:syncregistration._SyncProviderConfiguration
title: "_SyncProviderConfiguration"
author: windows-sdk-content
description: Represents the information for a synchronization provider configuration.
old-location: winsync\syncproviderconfiguration.htm
old-project: winsync
ms.assetid: 2b8c9a94-4e11-4904-a6aa-da0433d5b237
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: SyncProviderConfiguration, SyncProviderConfiguration structure [Windows Sync], _SyncProviderConfiguration, syncregistration/SyncProviderConfiguration, winsync.syncproviderconfiguration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SyncProviderConfiguration
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Syncregistration.h
api_name:
-	SyncProviderConfiguration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _SyncProviderConfiguration structure


## -description


Represents the information for a synchronization provider configuration. This structure is passed to the <a href="ISyncProviderRegistration::CreateSyncProviderRegistrationInstance">ISyncProviderRegistration::CreateSyncProviderRegistrationInstance</a> method when a registration instance is created.


## -struct-fields




### -field dwVersion

The xersion of the synchronization provider. The constant value <b>SYNC_PROVIDER_CONFIGURATION_VERSION.</b>


### -field guidInstanceId

The unique instance ID of the synchronization provider.


### -field clsidProvider

The COM CLSID of the synchronization provider.


### -field guidConfigUIInstanceId

The instance ID of the configuration UI  used to create this synchronization provider, or <b>GUID_NULL</b> if no configuration UI was used.


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
<li><b>SYNC_64_BIT_SUPPORTED</b>  ((DWORD)0x00000002)</li>
</ul>

## -see-also




<a href="https://msdn.microsoft.com/d514d0ed-6e99-4a11-a681-2844fced0347">Windows Sync Registration Structures</a>
 

 

