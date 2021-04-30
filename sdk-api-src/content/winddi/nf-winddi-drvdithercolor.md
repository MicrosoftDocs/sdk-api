---
UID: NF:winddi.DrvDitherColor
title: DrvDitherColor function (winddi.h)
description: The DrvDitherColor function requests the device to create a brush dithered against a device palette.
helpviewer_keywords: ["DrvDitherColor","DrvDitherColor function [Display Devices]","ddifncs_2b62d877-2c36-41ad-bca7-88f1daf3640c.xml","display.drvdithercolor","winddi/DrvDitherColor"]
old-location: display\drvdithercolor.htm
tech.root: display
ms.assetid: 635a4af8-ec19-4f99-80b2-bad2a6e87edc
ms.date: 12/05/2018
ms.keywords: DrvDitherColor, DrvDitherColor function [Display Devices], ddifncs_2b62d877-2c36-41ad-bca7-88f1daf3640c.xml, display.drvdithercolor, winddi/DrvDitherColor
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
 - DrvDitherColor
 - winddi/DrvDitherColor
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
 - DrvDitherColor
---

# DrvDitherColor function


## -description

The <b>DrvDitherColor</b> function requests the device to create a brush dithered against a device palette.

## -parameters

### -param dhpdev [in]

Handle to the PDEV structure that describes the physical device against whose palettes the specified color should be dithered.

### -param iMode [in]

Determines the palette to dither against. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DM_DEFAULT

</td>
<td>
The driver should create a dither for the native, default color space of the device. For example, if the device is running at 16bpp, the resulting dither should be in a 16bpp format. 

</td>
</tr>
<tr>
<td>
DM_MONOCHROME

</td>
<td>
The driver should create the dither for monochrome color space; that is, the dither should be returned as a 1bpp bitmap.

</td>
</tr>
</table>

### -param rgb [in]

Specifies the RGB color that is to be dithered.

### -param pul [in, out]

Pointer to the memory location that receives the dithering information. Memory must have been allocated for a standard-format bitmap with dithered brush dimensions <b>cxDither</b> by <b>cyDither</b>. These dimensions are members of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure. The bitmap format is determined by the <b>iDitherFormat</b> member of the DEVINFO structure.

## -returns

The return value is DCR_DRIVER if the dither values have been calculated by the driver, DCR_SOLID if the engine should use the best solid color approximation of the color, or DCR_HALFTONE if the engine should create a halftone approximation for the driver.

## -remarks

The result of the dither is a set of device color indices stored in <i>pul</i>. A brush created using these colors for its pattern should be a good approximation of the given color <i>rgb</i>.

<i>DrvDitherColor</i> is an optional function that is called only if <b>cxDither</b> and <b>cyDither</b> are nonzero. Monochrome device drivers, including most raster printers, should use the <i>iMode</i> parameter to tell GDI how to get good gray-scale patterns.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>