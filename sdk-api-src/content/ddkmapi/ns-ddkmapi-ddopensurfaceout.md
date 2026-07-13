---
UID: NS:ddkmapi._DDOPENSURFACEOUT
title: DDOPENSURFACEOUT (ddkmapi.h)
description: The DDOPENSURFACEOUT structure contains a new DirectDrawSurface handle, if the ddRVal member of DDOPENSURFACEOUT is set to DD_OK. This new handle must be used on all subsequent calls that require a DirectDrawSurface handle.
helpviewer_keywords: ["*LPDDOPENSURFACEOUT","DDOPENSURFACEOUT","DDOPENSURFACEOUT structure [Display Devices]","LPDDOPENSURFACEOUT","LPDDOPENSURFACEOUT structure pointer [Display Devices]","ddkmapi/DDOPENSURFACEOUT","ddkmapi/LPDDOPENSURFACEOUT","ddstrcts_911314a4-692d-4909-9c30-e868a767e031.xml","display.ddopensurfaceout"]
old-location: display\ddopensurfaceout.htm
tech.root: display
ms.assetid: 0cf0db38-f512-4ca1-a386-5544a1c9433e
ms.date: 12/05/2018
ms.keywords: '*LPDDOPENSURFACEOUT, DDOPENSURFACEOUT, DDOPENSURFACEOUT structure [Display Devices], LPDDOPENSURFACEOUT, LPDDOPENSURFACEOUT structure pointer [Display Devices], ddkmapi/DDOPENSURFACEOUT, ddkmapi/LPDDOPENSURFACEOUT, ddstrcts_911314a4-692d-4909-9c30-e868a767e031.xml, display.ddopensurfaceout'
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
req.typenames: DDOPENSURFACEOUT, *LPDDOPENSURFACEOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDOPENSURFACEOUT
 - ddkmapi/_DDOPENSURFACEOUT
 - LPDDOPENSURFACEOUT
 - ddkmapi/LPDDOPENSURFACEOUT
 - DDOPENSURFACEOUT
 - ddkmapi/DDOPENSURFACEOUT
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
 - DDOPENSURFACEOUT
---

# DDOPENSURFACEOUT structure


## -description

The DDOPENSURFACEOUT structure contains a new DirectDrawSurface handle, if the <b>ddRVal</b> member of DDOPENSURFACEOUT is set to DD_OK. This new handle must be used on all subsequent calls that require a DirectDrawSurface handle.

## -struct-fields

### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a> function for <a href="/previous-versions/windows/hardware/drivers/ff550711(v=vs.85)">DD_DXAPI_OPENSURFACE</a> operations. A return code of DD_OK indicates success.

### -field hSurface

Handle to the new DirectDrawSurface object.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550711(v=vs.85)">DD_DXAPI_OPENSURFACE</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>