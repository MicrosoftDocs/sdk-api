---
UID: NF:winddi.DrvPlgBlt
title: DrvPlgBlt function (winddi.h)
description: The DrvPlgBlt function provides rotate bit-block transfer capabilities between combinations of device-managed and GDI-managed surfaces.
helpviewer_keywords: ["DrvPlgBlt","DrvPlgBlt function [Display Devices]","ddifncs_7ede9dd6-c295-42b1-96f0-966ce103cc2e.xml","display.drvplgblt","winddi/DrvPlgBlt"]
old-location: display\drvplgblt.htm
tech.root: display
ms.assetid: 5bd478f1-0c01-4d7f-9ed1-af84e5bbe773
ms.date: 12/05/2018
ms.keywords: DrvPlgBlt, DrvPlgBlt function [Display Devices], ddifncs_7ede9dd6-c295-42b1-96f0-966ce103cc2e.xml, display.drvplgblt, winddi/DrvPlgBlt
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
 - DrvPlgBlt
 - winddi/DrvPlgBlt
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
 - DrvPlgBlt
---

# DrvPlgBlt function


## -description

The <b>DrvPlgBlt</b> function provides rotate bit-block transfer capabilities between combinations of device-managed and GDI-managed surfaces.

## -parameters

### -param psoTrg [in, out]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to draw.

### -param psoSrc [in, out]

Pointer to a SURFOBJ structure that describes the source for the bit-block transfer operation.

### -param psoMsk [in, optional]

Pointer to an optional SURFOBJ structure that represents a mask for the source. It is defined by a logic map, which is a bitmap with one bit per pixel.

This mask limits the area of the source that is copied. A mask has an implicit <i>rop4</i> of 0xCCAA, which means the source should be copied wherever the mask is one, but the destination should be left alone wherever the mask is zero.

If this parameter is <b>NULL</b>, <i>rop4</i> is implicitly 0xCCCC, which means the source should be copied everywhere in the source rectangle.

The mask is always large enough to contain the relevant source; tiling is unnecessary.

### -param pco [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that limits the area of the destination to be modified. GDI functions enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles.

Whenever possible, GDI simplifies the clipping involved. Unlike the <a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a> function, <b>DrvPlgBlt</b> can be called with a single clipping rectangle. This prevents rounding errors in clipping the output.

### -param pxlo [in, optional]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that defines how color indices are translated between the source and target surfaces. The XLATEOBJ can also be queried to find the RGB color for any source index. If <i>pxlo</i> is <b>NULL</b>, no translation is needed.

A high quality rotate bit-block transfer is needed to interpolate colors.

### -param pca [in, optional]

Pointer to a COLORADJUSTMENT structure that defines the color adjustment values to be applied to the source bitmap before stretching the bits. For more information about this structure, see the Microsoft Windows SDK documentation.

### -param pptlBrushOrg [in, optional]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure that indicates the origin of the halftone brush. Device drivers that use halftone brushes should align the upper left pixel of the brush's pattern with this point on the device surface.

### -param pptfx [in]

Pointer to three POINTFIX structures that define a parallelogram in the destination surface. Define <i>pptfx</i>[0] as A, <i>pptfx</i>[1] as B, and <i>pptfx</i>[2] as C. A, B, and C define three vertices of a parallelogram. A fourth implicit vertex is given as:


```
    D = B + C − A
```


<b>DrvPlgBlt</b> is never called with A, B, and C collinear.

### -param prcl [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that defines the area to be copied, in the coordinate system of the source surface. The points of the source rectangle are well ordered. <b>DrvPlgBlt</b> will never be given an empty source rectangle.

### -param pptl [in, optional]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that specifies which pixel in the given mask corresponds to the upper-left pixel in the source rectangle. Ignore this parameter if no <i>psoMsk</i> is specified.

### -param iMode [in]

Defines how source pixels are combined to get output pixels. This value can be one of the following:

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
On a shrinking bit-block transfer, pixels should be combined with an AND operation. On a stretching bit-block transfer, pixels should be replicated.

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
The driver can use groups of pixels in the output surface to best approximate the color or gray level of the input.

</td>
</tr>
<tr>
<td>
WHITEONBLACK

</td>
<td>
On a shrinking bit-block transfer, pixels should be combined with an OR operation. On a stretching bit-block transfer, pixels should be replicated.

</td>
</tr>
</table>
 

The methods WHITEONBLACK, BLACKONWHITE, and COLORONCOLOR provide compatibility for old applications, but do not produce the best results for color surfaces.

## -returns

<b>DrvPlgBlt</b> returns <b>TRUE</b> upon success. Otherwise, it reports an error and returns <b>FALSE</b>.

## -remarks

Similar to <a href="/windows/desktop/api/winddi/nf-winddi-drvstretchblt">DrvStretchBlt</a>, <b>DrvPlgBlt</b> enables a device driver to write to GDI bitmaps, especially when the driver can do halftoning.

To transform the bitmap, this function performs bit-block transfers from a rectangle defined by <i>prcl</i> to any parallelogram. The parallelogram is defined by <i>pptfx</i>, which points to an array of three points.

The source rectangle at <i>prcl</i> is considered to be a geometric rectangle whose corners are displaced by (-0.5,-0.5) from the given integer coordinates. This exactly matches the source rectangle for <a href="/windows/desktop/api/winddi/nf-winddi-drvstretchblt">DrvStretchBlt</a>. The source rectangle is always well ordered.

The upper-left corner of the source rectangle is mapped to the first point, A. The upper-right corner of the source rectangle is mapped to the second point, B. The lower-left corner of the source rectangle is mapped to the third point, C. The lower right corner of the source rectangle is mapped to the implicit point in the parallelogram defined by treating the three given points as vectors and computing:


```
    D = B + C - A
```


Note that a stretch blt can be expressed exactly as a parallelogram blt, but the coordinates given for the destination will have a fractional part of 0.5.

<b>DrvPlgBlt</b> is optional for graphics drivers. It is provided only for certain types of rotation. The driver should call <a href="/windows/desktop/api/winddi/nf-winddi-engplgblt">EngPlgBlt</a> if <b>DrvPlgBlt</b> is called to perform operations it does not support.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvalphablend">DrvAlphaBlend</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstretchblt">DrvStretchBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstretchbltrop">DrvStretchBltROP</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvtransparentblt">DrvTransparentBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engalphablend">EngAlphaBlend</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engbitblt">EngBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engplgblt">EngPlgBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engstretchblt">EngStretchBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engstretchbltrop">EngStretchBltROP</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engtransparentblt">EngTransparentBlt</a>