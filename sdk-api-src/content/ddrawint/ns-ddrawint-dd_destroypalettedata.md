---
UID: NS:ddrawint._DD_DESTROYPALETTEDATA
title: DD_DESTROYPALETTEDATA (ddrawint.h)
description: The DD_DESTROYPALETTEDATA structure contains information necessary to destroy the specified palette.
helpviewer_keywords: ["*PDD_DESTROYPALETTEDATA","DD_DESTROYPALETTEDATA","DD_DESTROYPALETTEDATA structure [Display Devices]","ddrawint/DD_DESTROYPALETTEDATA","ddstrcts_850bb816-b0df-4877-8903-c85b15074e30.xml","display.dd_destroypalettedata"]
old-location: display\dd_destroypalettedata.htm
tech.root: display
ms.assetid: e309f782-bd0b-4703-b58c-e202fd87b904
ms.date: 12/05/2018
ms.keywords: '*PDD_DESTROYPALETTEDATA, DD_DESTROYPALETTEDATA, DD_DESTROYPALETTEDATA structure [Display Devices], ddrawint/DD_DESTROYPALETTEDATA, ddstrcts_850bb816-b0df-4877-8903-c85b15074e30.xml, display.dd_destroypalettedata'
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
req.typenames: '*PDD_DESTROYPALETTEDATA, DD_DESTROYPALETTEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_DESTROYPALETTEDATA
 - ddrawint/_DD_DESTROYPALETTEDATA
 - PDD_DESTROYPALETTEDATA
 - ddrawint/PDD_DESTROYPALETTEDATA
 - DD_DESTROYPALETTEDATA
 - ddrawint/DD_DESTROYPALETTEDATA
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
 - DD_DESTROYPALETTEDATA
---

# DD_DESTROYPALETTEDATA structure


## -description

The DD_DESTROYPALETTEDATA structure contains information necessary to destroy the specified palette.

## -struct-fields

### -field lpDD

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDPalette

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palette_global">DD_PALETTE_GLOBAL</a> structure representing the palette object to be destroyed.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_palcb_destroypalette">DdDestroyPalette</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field DestroyPalette

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_palcb_destroypalette">DdDestroyPalette</a>