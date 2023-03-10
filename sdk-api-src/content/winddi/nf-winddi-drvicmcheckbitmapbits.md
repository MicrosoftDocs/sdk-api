---
UID: NF:winddi.DrvIcmCheckBitmapBits
title: DrvIcmCheckBitmapBits function (winddi.h)
description: The DrvIcmCheckBitmapBits function checks whether the pixels in the specified bitmap lie within the device gamut of the specified transform.
helpviewer_keywords: ["DrvIcmCheckBitmapBits","DrvIcmCheckBitmapBits function [Display Devices]","ddifncs_f7d444c6-446a-4c46-9f5e-73407323c2d7.xml","display.drvicmcheckbitmapbits","winddi/DrvIcmCheckBitmapBits"]
old-location: display\drvicmcheckbitmapbits.htm
tech.root: display
ms.assetid: afde9270-3bbf-4f78-97ca-20ddfae83a2d
ms.date: 12/05/2018
ms.keywords: DrvIcmCheckBitmapBits, DrvIcmCheckBitmapBits function [Display Devices], ddifncs_f7d444c6-446a-4c46-9f5e-73407323c2d7.xml, display.drvicmcheckbitmapbits, winddi/DrvIcmCheckBitmapBits
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
 - DrvIcmCheckBitmapBits
 - winddi/DrvIcmCheckBitmapBits
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
 - DrvIcmCheckBitmapBits
---

# DrvIcmCheckBitmapBits function


## -description

The <b>DrvIcmCheckBitmapBits</b> function checks whether the pixels in the specified bitmap lie within the device gamut of the specified transform.

## -parameters

### -param dhpdev

Handle to the physical device's <a href="/windows-hardware/drivers/">PDEV</a>.

### -param hColorTransform

Handle to the color transform against which the bitmap is to be checked. This transform was created by the driver through a prior call to its <a href="/windows/desktop/api/winddi/nf-winddi-drvicmcreatecolortransform">DrvIcmCreateColorTransform</a> routine.

### -param pso

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> that contains the bitmap surface to be checked.

### -param paResults

Pointer to an array of bytes in which the driver returns the test results. GDI allocates this buffer to contain at least as many bytes as there are pixels in the bitmap. The driver need not perform any allocation or bound checking before writing to the array.

## -returns

<b>DrvIcmCheckBitmapBits</b> returns <b>TRUE</b> upon success. Otherwise, it reports an error and returns <b>FALSE</b>.

## -remarks

Each byte in the array to which <i>paResults</i> points corresponds with a pixel in the bitmap. For each pixel, the driver determines whether its color value is in the device gamut and then writes a value between zero and 255 in the corresponding array byte. The values have the following meanings:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
Zero

</td>
<td>
The color is in the device gamut.

</td>
</tr>
<tr>
<td>
Nonzero

</td>
<td>
The color is outside of the gamut. A value of <i>n+1</i> indicates that the color is at least as far out of the gamut as a value of <i>n</i>.

</td>
</tr>
</table>
 

<b>DrvIcmCheckBitmapBits</b> can be optionally implemented in drivers that support ICM. A driver indicates support for ICM by setting the GCAPS_ICM flag in the <b>flGraphicsCaps</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvicmcreatecolortransform">DrvIcmCreateColorTransform</a>