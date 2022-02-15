---
UID: NF:winddi.DrvSetPalette
title: DrvSetPalette function (winddi.h)
description: The DrvSetPalette function requests that the driver realize the palette for a specified device.
helpviewer_keywords: ["DrvSetPalette","DrvSetPalette function [Display Devices]","ddifncs_b76ad321-743e-4e7b-bf58-85f969470e29.xml","display.drvsetpalette","winddi/DrvSetPalette"]
old-location: display\drvsetpalette.htm
tech.root: display
ms.assetid: b7be48e6-188b-4b23-a494-30adcc18f12e
ms.date: 12/05/2018
ms.keywords: DrvSetPalette, DrvSetPalette function [Display Devices], ddifncs_b76ad321-743e-4e7b-bf58-85f969470e29.xml, display.drvsetpalette, winddi/DrvSetPalette
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvSetPalette
 - winddi/DrvSetPalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvSetPalette
---

# DrvSetPalette function


## -description

The <b>DrvSetPalette</b> function requests that the driver realize the palette for a specified device.

## -parameters

### -param dhpdev

Handle to the physical device's <a href="/windows-hardware/drivers/">PDEV</a> structure, which identifies the device whose palette is to be realized. This parameter is the device handle returned to GDI by <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>.

### -param ppalo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-palobj">PALOBJ</a> structure from which the colors (RGB values) should be queried.

### -param fl

A set of flags that provides hints and options. This parameter can be the following value:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
SP_DEFAULT

</td>
<td>
The palette is the device's complete default palette. The <a href="/windows/desktop/api/winddi/ns-winddi-palobj">PALOBJ</a> can be ignored, but contains the correct contents.

</td>
</tr>
</table>

### -param iStart

Specifies the first palette index to overwrite.

### -param cColors

Specifies the number of colors to change in the hardware palette. Extra colors, beyond the number available in the hardware, can be ignored. If <i>cColors</i> is smaller than the size of the hardware palette, set only <i>cColors</i> entries and leave the remaining colors as they are.

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.

## -remarks

 The driver sets the hardware palette to match the entries in the given palette as closely as possible.

Only indexed palettes are realizable. The RC_PALETTE bit of the <b>flRasterCaps</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a> structure specifies whether a device has a realizable palette.

<b>DrvSetPalette</b> is required for display drivers that support realizable palettes.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatepalette">EngCreatePalette</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeletepalette">EngDeletePalette</a>