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

# D2D1_RENDER_TARGET_TYPE enumeration


## -description


Describes whether a render target uses hardware or software rendering, or if Direct2D should select the rendering mode.


## -enum-fields




### -field D2D1_RENDER_TARGET_TYPE_DEFAULT

The render target uses hardware rendering, if available; otherwise, it uses software rendering.


### -field D2D1_RENDER_TARGET_TYPE_SOFTWARE

The render target uses software rendering only.


### -field D2D1_RENDER_TARGET_TYPE_HARDWARE

The render target uses hardware rendering only. 


### -field D2D1_RENDER_TARGET_TYPE_FORCE_DWORD




## -remarks



Not every render target supports hardware rendering. For more information, see the <a href="https://msdn.microsoft.com/8a67babd-20c7-47f4-8dd3-8c0320d89ad6">Render Targets Overview</a>. 




## -see-also




<a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a>



<a href="https://msdn.microsoft.com/8a67babd-20c7-47f4-8dd3-8c0320d89ad6">Render Targets Overview</a>
 

 

