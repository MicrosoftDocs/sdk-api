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

# _DDGETAUTOFLIPOUT structure


## -description


The DDGETAUTOFLIPOUT structure contains the handle and polarity information returned from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550642">DD_DXAPI_GET_CURRENT_VP_AUTOFLIP_SURFACE</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff550650">DD_DXAPI_GET_LAST_VP_AUTOFLIP_SURFACE</a> function identifiers of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a> function. 


## -struct-fields




### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a> function for operations that obtain autoflip surfaces. Contains DD_OK if the hardware video port is in autoflip mode.


### -field hVideoSurface

Handle for the current video surface.


### -field hVBISurface

Handle for the current <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VBI</a> data.


### -field bPolarity

Specifies whether the field is an even or odd field of an interlaced video signal. This member should be set to <b>TRUE</b> if the current field is the even field and to <b>FALSE</b> if the current field is the odd field.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550642">DD_DXAPI_GET_CURRENT_VP_AUTOFLIP_SURFACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550650">DD_DXAPI_GET_LAST_VP_AUTOFLIP_SURFACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

