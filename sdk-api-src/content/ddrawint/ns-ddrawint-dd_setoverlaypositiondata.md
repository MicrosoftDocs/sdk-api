---
UID: NS:ddrawint._DD_SETOVERLAYPOSITIONDATA
title: DD_SETOVERLAYPOSITIONDATA (ddrawint.h)
description: The DD_SETOVERLAYPOSITIONDATA structure contains information necessary to change the display coordinates of an overlay surface.
helpviewer_keywords: ["*PDD_SETOVERLAYPOSITIONDATA","DD_SETOVERLAYPOSITIONDATA","DD_SETOVERLAYPOSITIONDATA structure [Display Devices]","ddrawint/DD_SETOVERLAYPOSITIONDATA","ddstrcts_963680b2-05c1-4f15-959c-c38a8141541b.xml","display.dd_setoverlaypositiondata"]
old-location: display\dd_setoverlaypositiondata.htm
tech.root: display
ms.assetid: edfcbe23-81af-41fb-b29e-cd6e2da4d603
ms.date: 12/05/2018
ms.keywords: '*PDD_SETOVERLAYPOSITIONDATA, DD_SETOVERLAYPOSITIONDATA, DD_SETOVERLAYPOSITIONDATA structure [Display Devices], ddrawint/DD_SETOVERLAYPOSITIONDATA, ddstrcts_963680b2-05c1-4f15-959c-c38a8141541b.xml, display.dd_setoverlaypositiondata'
req.header: ddrawint.h
req.include-header: Winddi.h
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
req.typenames: '*PDD_SETOVERLAYPOSITIONDATA, DD_SETOVERLAYPOSITIONDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_SETOVERLAYPOSITIONDATA
 - ddrawint/_DD_SETOVERLAYPOSITIONDATA
 - PDD_SETOVERLAYPOSITIONDATA
 - ddrawint/PDD_SETOVERLAYPOSITIONDATA
 - DD_SETOVERLAYPOSITIONDATA
 - ddrawint/DD_SETOVERLAYPOSITIONDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_SETOVERLAYPOSITIONDATA
---

# DD_SETOVERLAYPOSITIONDATA structure


## -description

The DD_SETOVERLAYPOSITIONDATA structure contains information necessary to change the display coordinates of an overlay surface.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDSrcSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that represents the Microsoft DirectDraw overlay surface.

### -field lpDDDestSurface

Points to a DD_SURFACE_LOCAL structure representing the surface that is being overlaid.

### -field lXPos

Specifies the x-coordinate of the upper left corner of the overlay, in pixels.

### -field lYPos

Specifies the y coordinate of the upper left corner of the overlay, in pixels.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setoverlayposition">DdSetOverlayPosition</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field SetOverlayPosition

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setoverlayposition">DdSetOverlayPosition</a>