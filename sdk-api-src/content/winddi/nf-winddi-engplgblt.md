---
UID: NF:winddi.EngPlgBlt
title: EngPlgBlt function (winddi.h)
description: The EngPlgBlt function causes GDI to perform a rotate bit-block transfer.
helpviewer_keywords: ["EngPlgBlt","EngPlgBlt function [Display Devices]","display.engplgblt","gdifncs_e7b5fc87-c1d3-4513-a101-742cd358ed85.xml","winddi/EngPlgBlt"]
old-location: display\engplgblt.htm
tech.root: display
ms.assetid: a25a0fcd-1a61-483a-ba22-1214a9806b70
ms.date: 12/05/2018
ms.keywords: EngPlgBlt, EngPlgBlt function [Display Devices], display.engplgblt, gdifncs_e7b5fc87-c1d3-4513-a101-742cd358ed85.xml, winddi/EngPlgBlt
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngPlgBlt
 - winddi/EngPlgBlt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-common-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngPlgBlt
---

# EngPlgBlt function


## -description

The <b>EngPlgBlt</b> function causes GDI to perform a rotate bit-block transfer.

## -parameters

### -param psoTrg

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to draw.

### -param psoSrc

Pointer to a SURFOBJ structure that describes the source surface for the bit-block transfer operation.

### -param psoMsk

Pointer to an optional SURFOBJ structure that represents a mask for the source. It is defined by a logic map, which is a bitmap with one bit per pixel.

This mask limits the area of the source that is copied. A mask has an implicit <i>rop4</i> of 0xCCAA, which means the source should be copied wherever the mask is 1, but the destination should be left alone wherever the mask is zero.

If this parameter is <b>NULL</b>, there is an implicit <i>rop4</i> of 0xCCCC, which means the source should be copied everywhere in the source rectangle.

The mask will always be large enough to contain the relevant source; tiling is unnecessary.

### -param pco

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that limits the area of the destination to be modified. GDI functions enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles.

Whenever possible, GDI simplifies the clipping involved. Unlike the <a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a> function, <b>EngPlgBlt</b> may be called with a single clipping rectangle. This prevents rounding errors in clipping the output.

### -param pxlo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that defines how color indices are translated between the source and target surfaces. This XLATEOBJ structure can be queried to find the RGB color for any source index.

A high quality rotate bit-block transfer is needed to interpolate colors.

### -param pca

Pointer to a COLORADJUSTMENT structure that defines the color adjustment values to be applied to the source bitmap before stretching the bits. For more information, see the Microsoft Windows SDK documentation.

### -param pptlBrushOrg

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that specifies the origin of the halftone brush. Drivers that use halftone brushes should align the upper left pixel of the brush's pattern with this point on the device surface.

### -param pptfx

Pointer to three POINTFIX structures that define a parallelogram in the destination surface. A fourth, implicit, vertex is given as: D = B + C − A. For a description of this data type, see <a href="/windows-hardware/drivers/display/gdi-data-types">GDI Data Types</a>.

<b>EngPlgBlt</b> is never called with A, B, and C collinear.

### -param prcl

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that defines, in the coordinate system of the source surface, the area to be copied. The points of the source rectangle are well ordered. <b>EngPlgBlt</b> will never be given an empty source rectangle.

### -param pptl

Pointer to a POINTL structure that specifies which pixel in the given mask corresponds to the upper-left pixel in the source rectangle. Ignore this parameter if <i>psoMsk</i> is <b>NULL</b>.

### -param iMode [in]

Defines how source pixels are combined to get output pixels. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
BLACKONWHITE

</td>
<td>
On a shrinking bit-block transfer, pixels should be combined with an AND operation. On a stretching bit-block transfer pixels should be replicated.

</td>
</tr>
<tr>
<td>
COLORONCOLOR

</td>
<td>
On a shrinking bit-block transfer, enough pixels should be ignored so that pixels need not be combined. On a stretching bit-block transfer, pixels should be replicated.

</td>
</tr>
<tr>
<td>
HALFTONE

</td>
<td>
The driver may use groups of pixels in the output surface to best approximate the color or gray level of the input.

</td>
</tr>
<tr>
<td>
WHITEONBLACK

</td>
<td>
On a shrinking bit-block transfer, pixels should be combined with an OR operation. On a stretching block transfers, pixels should be replicated.

</td>
</tr>
</table>
 

The methods WHITEONBLACK, BLACKONWHITE, and COLORONCOLOR are simple and provide compatibility for old applications, but do not produce the best looking results for color surfaces.

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b> and an error code is reported.

## -remarks

<b>EngPlgBlt</b> performs only certain types of rotations.

This function performs bit-block transfers from a rectangle defined by <i>prcl</i> to any parallelogram. The parallelogram is defined by <i>pptfx</i>, which points to an array of three points.

The source rectangle at <i>prcl</i> is considered to be a geometric rectangle whose corners are displaced by (-0.5,-0.5) from the given integer coordinates. This exactly matches the source rectangle for <a href="/windows/desktop/api/winddi/nf-winddi-engstretchblt">EngStretchBlt</a>. The source rectangle is always well ordered.

The upper-left corner of the source rectangle is mapped to the first point, A. The upper-right corner of the source rectangle is mapped to the second point, B. The lower-left corner of the source rectangle is mapped to the third point, C. The lower-right corner of the source rectangle is mapped to the implicit point in the parallelogram defined by treating the three given points as vectors and computing:


```
D = B + C - A
```


Note that a stretch blit can be expressed exactly as a parallelogram blit, but the coordinates given for the destination will be divisible by five.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvalphablend">DrvAlphaBlend</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvplgblt">DrvPlgBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstretchblt">DrvStretchBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstretchbltrop">DrvStretchBltROP</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvtransparentblt">DrvTransparentBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engalphablend">EngAlphaBlend</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engbitblt">EngBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engstretchblt">EngStretchBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engstretchbltrop">EngStretchBltROP</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engtransparentblt">EngTransparentBlt</a>