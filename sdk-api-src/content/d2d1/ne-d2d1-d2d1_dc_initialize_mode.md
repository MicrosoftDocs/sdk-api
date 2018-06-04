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

# D2D1_DC_INITIALIZE_MODE enumeration


## -description


 Specifies how a device context is initialized for GDI rendering when it is retrieved from the render target.


## -enum-fields




### -field D2D1_DC_INITIALIZE_MODE_COPY

The current contents of the render target are copied to the device context when it is initialized. 


### -field D2D1_DC_INITIALIZE_MODE_CLEAR

The device context is cleared to transparent black when it is initialized.


### -field D2D1_DC_INITIALIZE_MODE_FORCE_DWORD




## -remarks



Use this enumeration with the <a href="https://msdn.microsoft.com/40797258-84a0-44ee-8b64-04ceb3eb1998">ID2D1GdiInteropRenderTarget::GetDC</a> method to specify how the device context is  initialized for GDI rendering.




## -see-also




<a href="https://msdn.microsoft.com/40797258-84a0-44ee-8b64-04ceb3eb1998">ID2D1GdiInteropRenderTarget::GetDC</a>
 

 

