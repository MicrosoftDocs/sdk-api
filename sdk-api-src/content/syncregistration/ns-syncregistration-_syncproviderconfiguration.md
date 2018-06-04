---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

