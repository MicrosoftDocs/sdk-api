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

# _DDOPENSURFACEIN structure


## -description


The DDOPENSURFACEIN structure contains the DirectDrawSurface object information. 


## -struct-fields




### -field hDirectDraw

Specifies the Microsoft DirectDraw object to which the surface handle is associated.


### -field dwSurfaceHandle

Specifies the DirectDrawSurface handle passed down from user mode.


### -field pfnSurfaceClose

Points to a <a href="https://msdn.microsoft.com/ee581d7b-c3b8-47e5-bae8-348b22ea0f95">pfnSurfaceClose</a> callback function that is called when the surface becomes unusable.


### -field pContext

Contains a value that is passed if the <b>pfnSurfaceClose</b> callback function is ever called.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550711">DD_DXAPI_OPENSURFACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

