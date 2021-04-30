---
UID: NS:ddrawint._DD_CREATEPALETTEDATA
title: DD_CREATEPALETTEDATA (ddrawint.h)
description: The DD_CREATEPALETTEDATA structure contains information necessary to create a DirectDrawPalette object for this Microsoft DirectDraw object.
helpviewer_keywords: ["*PDD_CREATEPALETTEDATA","DD_CREATEPALETTEDATA","DD_CREATEPALETTEDATA structure [Display Devices]","ddrawint/DD_CREATEPALETTEDATA","ddstrcts_9370d793-ebdf-47ef-bc5f-869906c6e20a.xml","display.dd_createpalettedata"]
old-location: display\dd_createpalettedata.htm
tech.root: display
ms.assetid: e43ad510-b44b-4a4d-abb2-10062ce69140
ms.date: 12/05/2018
ms.keywords: '*PDD_CREATEPALETTEDATA, DD_CREATEPALETTEDATA, DD_CREATEPALETTEDATA structure [Display Devices], ddrawint/DD_CREATEPALETTEDATA, ddstrcts_9370d793-ebdf-47ef-bc5f-869906c6e20a.xml, display.dd_createpalettedata'
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
req.typenames: '*PDD_CREATEPALETTEDATA, DD_CREATEPALETTEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_CREATEPALETTEDATA
 - ddrawint/_DD_CREATEPALETTEDATA
 - PDD_CREATEPALETTEDATA
 - ddrawint/PDD_CREATEPALETTEDATA
 - DD_CREATEPALETTEDATA
 - ddrawint/DD_CREATEPALETTEDATA
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
 - DD_CREATEPALETTEDATA
---

# DD_CREATEPALETTEDATA structure


## -description

The DD_CREATEPALETTEDATA structure contains information necessary to create a DirectDrawPalette object for this Microsoft DirectDraw object.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDPalette

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palette_global">DD_PALETTE_GLOBAL</a> structure representing the DirectDrawPalette object.

### -field lpColorTable

Points to an array of 2, 4, 16, or 256 PALETTEENTRY structures used to initialize the colors for this DirectDrawPalette object. See the latest Microsoft DirectX SDK documentation for more information about PALETTEENTRY.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createpalette">DdCreatePalette</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field CreatePalette

Used by the DirectDraw API and should not be filled in by the driver.

### -field is_excl

Specifies a BOOL value that is set to <b>TRUE</b> to indicate that this process has exclusive mode and <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createpalette">DdCreatePalette</a>