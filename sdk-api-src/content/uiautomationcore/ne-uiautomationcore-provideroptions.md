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

# ProviderOptions enumeration


## -description


Contains values that specify the type of UI Automation provider. The <a href="https://msdn.microsoft.com/fd41bb43-bbf1-4022-9472-0ad2816074c6">IRawElementProviderSimple::ProviderOptions</a> property uses this enumeration.


## -enum-fields




### -field ProviderOptions_ClientSideProvider

The provider is a client-side (proxy) provider.


### -field ProviderOptions_ServerSideProvider

The provider is a server-side provider.


### -field ProviderOptions_NonClientAreaProvider

The provider is a non-client-area provider.  


### -field ProviderOptions_OverrideProvider

The provider overrides another provider.


### -field ProviderOptions_ProviderOwnsSetFocus

The provider handles its own focus, and does not want UI Automation to set focus to the nearest window on its behalf. This option is typically used by providers for windows that appear to take focus without actually receiving Win32 focus, such as menus and drop-downs. 


### -field ProviderOptions_UseComThreading

The provider has explicit support for COM threading models, so that calls by UI Automation on COM-based providers are received on the appropriate thread. This means that STA-based provider implementations will be called back on their own STA thread, and therefore do not need extra synchronization to safely access resources that belong to that STA. MTA-based provider implementations will be called back on some other thread in the MTA, and will require appropriate synchronization to be added, as is usual for MTA code.


### -field ProviderOptions_RefuseNonClientSupport

The provider handles its own non-client area and does not want UI Automation to provide default accessibility support for controls in the non-client area, such as minimize/maximize buttons and menu bars.


### -field ProviderOptions_HasNativeIAccessible

The provider implements the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface. 


### -field ProviderOptions_UseClientCoordinates

The provider works in client coordinates instead of screen coordinates.


## -see-also




<a href="https://msdn.microsoft.com/343959bc-42d0-4289-b507-7da78cee28f2">SetFocus</a>
 

 

