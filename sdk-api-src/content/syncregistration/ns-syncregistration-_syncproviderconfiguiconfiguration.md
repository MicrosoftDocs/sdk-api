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

# _SyncProviderConfigUIConfiguration structure


## -description


Represents the information for a synchronization provider configuration UI.


## -struct-fields




### -field dwVersion

The version of the configuration UI.


### -field guidInstanceId

The unique instance ID of the configuration UI.


### -field clsidConfigUI

The COM CLSID of the configuration UI.


### -field guidContentType

The GUID that identifies the content type supported by the synchronization provider that is created by the configuration UI.


### -field dwCapabilities

One of the following constants that represent the capabilities of the synchronization provider configuration UI. These values are masks that can be combined.

<ul>
<li><b>SCC_DEFAULT</b> ((DWORD)0x00000000) The configuration UI supports the default capabilities of creating and modifying a synchronization provider with a UI displayed.

</li>
<li><b>SCC_CAN_CREATE_WITHOUT_UI</b>  ((DWORD)0x00000001) The configuration UI creates providers without displaying the UI.  This value is not compatible with <b>SCC_CREATE_NOT_SUPPORTED</b>.

</li>
<li><b>SCC_CAN_MODIFY_WITHOUT_UI</b>  ((DWORD)0x00000002) The configuration UI modifies providers without displaying the UI.  This value is not compatible with <b>SCC_MODIFY_NOT_SUPPORTED</b>.

</li>
<li><b>SCC_CREATE_NOT_SUPPORTED</b>  ((DWORD)0x00000004) The configuration UI cannot create new configured providers.  This value is not compatible with <b>SCC_CAN_CREATE_WITHOUT_UI</b>.

</li>
<li><b>SCC_MODIFY_NOT_SUPPORTED</b>  ((DWORD)0x00000008) The configuration UI cannot modify providers.  This value is not compatible with <b>SCC_CAN_MODIFY_WITHOUT_UI</b>.

</li>
</ul>

### -field dwSupportedArchitecture

One of the following constants that represent the architectures supported by the synchronization provider configuration UI. This value corresponds to the architectures that the synchronization provider configuration UI CLSID (<b>clsidConfigUI</b>) is registered for.   These values can be combined, and can be used as bitmasks.

<ul>
<li><b>SYNC_32_BIT_SUPPORTED</b> ((DWORD)0x00000001)</li>
<li><b>SYNC_64_BIT_SUPPORTED</b>  ((DWORD)0x00000002)</li>
</ul>

### -field fIsGlobal

Reserved for future use. At this time, the value should always be <b>FALSE</b>.


## -see-also




<a href="https://msdn.microsoft.com/d514d0ed-6e99-4a11-a681-2844fced0347">Windows Sync Registration Structures</a>
 

 

