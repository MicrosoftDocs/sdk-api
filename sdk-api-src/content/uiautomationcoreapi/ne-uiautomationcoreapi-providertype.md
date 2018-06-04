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

# ProviderType enumeration


## -description


Contains values that specify the type of a client-side (proxy) UI Automation provider.


## -enum-fields




### -field ProviderType_BaseHwnd

The provider is window-based.


### -field ProviderType_Proxy

The provider is one of the Win32 or Windows Forms providers from Microsoft, or a third-party proxy provider.


### -field ProviderType_NonClientArea

The provider is a proxy for the window's non-client-area elements.

