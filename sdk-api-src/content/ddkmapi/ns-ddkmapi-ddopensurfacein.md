---
UID: NS:ddkmapi._DDOPENSURFACEIN
title: DDOPENSURFACEIN (ddkmapi.h)
description: The DDOPENSURFACEIN structure contains the DirectDrawSurface object information.
helpviewer_keywords: ["*LPDDOPENSURFACEIN","DDOPENSURFACEIN","DDOPENSURFACEIN structure [Display Devices]","LPDDOPENSURFACEIN","LPDDOPENSURFACEIN structure pointer [Display Devices]","ddkmapi/DDOPENSURFACEIN","ddkmapi/LPDDOPENSURFACEIN","ddstrcts_406539e4-c43f-4871-b00b-30c71433d1fd.xml","display.ddopensurfacein"]
old-location: display\ddopensurfacein.htm
tech.root: display
ms.assetid: 98a5d436-096d-4698-8f2c-31a0455300ff
ms.date: 12/05/2018
ms.keywords: '*LPDDOPENSURFACEIN, DDOPENSURFACEIN, DDOPENSURFACEIN structure [Display Devices], LPDDOPENSURFACEIN, LPDDOPENSURFACEIN structure pointer [Display Devices], ddkmapi/DDOPENSURFACEIN, ddkmapi/LPDDOPENSURFACEIN, ddstrcts_406539e4-c43f-4871-b00b-30c71433d1fd.xml, display.ddopensurfacein'
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
req.typenames: DDOPENSURFACEIN, *LPDDOPENSURFACEIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDOPENSURFACEIN
 - ddkmapi/_DDOPENSURFACEIN
 - LPDDOPENSURFACEIN
 - ddkmapi/LPDDOPENSURFACEIN
 - DDOPENSURFACEIN
 - ddkmapi/DDOPENSURFACEIN
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
 - DDOPENSURFACEIN
---

# DDOPENSURFACEIN structure


## -description

The DDOPENSURFACEIN structure contains the DirectDrawSurface object information.

## -struct-fields

### -field hDirectDraw

Specifies the Microsoft DirectDraw object to which the surface handle is associated.

### -field dwSurfaceHandle

Specifies the DirectDrawSurface handle passed down from user mode.

### -field pfnSurfaceClose

Points to a <a href="/windows/desktop/api/ddkmapi/nc-ddkmapi-lpdd_notifycallback">pfnSurfaceClose</a> callback function that is called when the surface becomes unusable.

### -field pContext

Contains a value that is passed if the <b>pfnSurfaceClose</b> callback function is ever called.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550711(v=vs.85)">DD_DXAPI_OPENSURFACE</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>