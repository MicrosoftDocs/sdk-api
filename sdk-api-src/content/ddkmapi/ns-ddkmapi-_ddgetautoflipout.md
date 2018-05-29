---
UID: NS:ddkmapi._DDGETAUTOFLIPOUT
title: "_DDGETAUTOFLIPOUT"
author: windows-sdk-content
description: The DDGETAUTOFLIPOUT structure contains the handle and polarity information returned from the DD_DXAPI_GET_CURRENT_VP_AUTOFLIP_SURFACE and DD_DXAPI_GET_LAST_VP_AUTOFLIP_SURFACE function identifiers of the DxApi function.
old-location: display\ddgetautoflipout.htm
old-project: display
ms.assetid: 48a64f86-9816-441d-9e4e-bd3f32d51728
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*LPDDGETAUTOFLIPOUT, DDGETAUTOFLIPOUT, DDGETAUTOFLIPOUT structure [Display Devices], LPDDGETAUTOFLIPOUT, LPDDGETAUTOFLIPOUT structure pointer [Display Devices], _DDGETAUTOFLIPOUT, ddkmapi/DDGETAUTOFLIPOUT, ddkmapi/LPDDGETAUTOFLIPOUT, ddstrcts_b11ef13a-2e8d-4676-b270-29b926abee91.xml, display.ddgetautoflipout"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
req.target-type: Windows
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
req.typenames: DDGETAUTOFLIPOUT, *LPDDGETAUTOFLIPOUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddkmapi.h
api_name:
-	DDGETAUTOFLIPOUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

