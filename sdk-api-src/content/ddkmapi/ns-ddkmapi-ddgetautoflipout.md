---
UID: NS:ddkmapi._DDGETAUTOFLIPOUT
title: DDGETAUTOFLIPOUT (ddkmapi.h)
description: The DDGETAUTOFLIPOUT structure contains the handle and polarity information returned from the DD_DXAPI_GET_CURRENT_VP_AUTOFLIP_SURFACE and DD_DXAPI_GET_LAST_VP_AUTOFLIP_SURFACE function identifiers of the DxApi function.
helpviewer_keywords: ["*LPDDGETAUTOFLIPOUT","DDGETAUTOFLIPOUT","DDGETAUTOFLIPOUT structure [Display Devices]","LPDDGETAUTOFLIPOUT","LPDDGETAUTOFLIPOUT structure pointer [Display Devices]","ddkmapi/DDGETAUTOFLIPOUT","ddkmapi/LPDDGETAUTOFLIPOUT","ddstrcts_b11ef13a-2e8d-4676-b270-29b926abee91.xml","display.ddgetautoflipout"]
old-location: display\ddgetautoflipout.htm
tech.root: display
ms.assetid: 48a64f86-9816-441d-9e4e-bd3f32d51728
ms.date: 12/05/2018
ms.keywords: '*LPDDGETAUTOFLIPOUT, DDGETAUTOFLIPOUT, DDGETAUTOFLIPOUT structure [Display Devices], LPDDGETAUTOFLIPOUT, LPDDGETAUTOFLIPOUT structure pointer [Display Devices], ddkmapi/DDGETAUTOFLIPOUT, ddkmapi/LPDDGETAUTOFLIPOUT, ddstrcts_b11ef13a-2e8d-4676-b270-29b926abee91.xml, display.ddgetautoflipout'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DDGETAUTOFLIPOUT, *LPDDGETAUTOFLIPOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGETAUTOFLIPOUT
 - ddkmapi/_DDGETAUTOFLIPOUT
 - LPDDGETAUTOFLIPOUT
 - ddkmapi/LPDDGETAUTOFLIPOUT
 - DDGETAUTOFLIPOUT
 - ddkmapi/DDGETAUTOFLIPOUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDGETAUTOFLIPOUT
---

# DDGETAUTOFLIPOUT structure


## -description

The DDGETAUTOFLIPOUT structure contains the handle and polarity information returned from the <a href="/previous-versions/windows/hardware/drivers/ff550642(v=vs.85)">DD_DXAPI_GET_CURRENT_VP_AUTOFLIP_SURFACE</a> and <a href="/previous-versions/windows/hardware/drivers/ff550650(v=vs.85)">DD_DXAPI_GET_LAST_VP_AUTOFLIP_SURFACE</a> function identifiers of the <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a> function.

## -struct-fields

### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a> function for operations that obtain autoflip surfaces. Contains DD_OK if the hardware video port is in autoflip mode.

### -field hVideoSurface

Handle for the current video surface.

### -field hVBISurface

Handle for the current <a href="/windows-hardware/drivers/">VBI</a> data.

### -field bPolarity

Specifies whether the field is an even or odd field of an interlaced video signal. This member should be set to <b>TRUE</b> if the current field is the even field and to <b>FALSE</b> if the current field is the odd field.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550642(v=vs.85)">DD_DXAPI_GET_CURRENT_VP_AUTOFLIP_SURFACE</a>



<a href="/previous-versions/windows/hardware/drivers/ff550650(v=vs.85)">DD_DXAPI_GET_LAST_VP_AUTOFLIP_SURFACE</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>