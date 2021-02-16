---
UID: NS:ddrawint._DD_SETPALETTEDATA
title: DD_SETPALETTEDATA (ddrawint.h)
description: The DD_SETPALETTEDATA structure contains information necessary to set a palette for a specific surface.
helpviewer_keywords: ["*PDD_SETPALETTEDATA","DD_SETPALETTEDATA","DD_SETPALETTEDATA structure [Display Devices]","ddrawint/DD_SETPALETTEDATA","ddstrcts_254301f1-b163-4402-92b2-70a2632f5ebc.xml","display.dd_setpalettedata"]
old-location: display\dd_setpalettedata.htm
tech.root: display
ms.assetid: 943af430-19b2-481a-9cac-cd4cb767d96a
ms.date: 12/05/2018
ms.keywords: '*PDD_SETPALETTEDATA, DD_SETPALETTEDATA, DD_SETPALETTEDATA structure [Display Devices], ddrawint/DD_SETPALETTEDATA, ddstrcts_254301f1-b163-4402-92b2-70a2632f5ebc.xml, display.dd_setpalettedata'
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
req.typenames: '*PDD_SETPALETTEDATA, DD_SETPALETTEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_SETPALETTEDATA
 - ddrawint/_DD_SETPALETTEDATA
 - PDD_SETPALETTEDATA
 - ddrawint/PDD_SETPALETTEDATA
 - DD_SETPALETTEDATA
 - ddrawint/DD_SETPALETTEDATA
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
 - DD_SETPALETTEDATA
---

# DD_SETPALETTEDATA structure


## -description

The DD_SETPALETTEDATA structure contains information necessary to set a palette for a specific surface.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that represents the DirectDrawSurface object.

### -field lpDDPalette

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palette_global">DD_PALETTE_GLOBAL</a> structure that specifies the palette to set to the surface.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setpalette">DdSetPalette</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field SetPalette

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

### -field Attach

Indicates whether to attach this palette to the surface.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setpalette">DdSetPalette</a>