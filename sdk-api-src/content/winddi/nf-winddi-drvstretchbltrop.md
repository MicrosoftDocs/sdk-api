---
UID: NF:winddi.DrvStretchBltROP
title: DrvStretchBltROP function (winddi.h)
description: The DrvStretchBltROP function performs a stretching bit-block transfer using a ROP.
helpviewer_keywords: ["DrvStretchBltROP","DrvStretchBltROP function [Display Devices]","ddifncs_c25f3aa6-9564-4189-b956-51cd2729576c.xml","display.drvstretchbltrop","winddi/DrvStretchBltROP"]
old-location: display\drvstretchbltrop.htm
tech.root: display
ms.assetid: eeaec7f4-2dfe-42a9-8789-a9ce11aec7b2
ms.date: 12/05/2018
ms.keywords: DrvStretchBltROP, DrvStretchBltROP function [Display Devices], ddifncs_c25f3aa6-9564-4189-b956-51cd2729576c.xml, display.drvstretchbltrop, winddi/DrvStretchBltROP
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
 - DrvStretchBltROP
 - winddi/DrvStretchBltROP
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
 - DrvStretchBltROP
---

# DrvStretchBltROP function


## -description

The <b>DrvStretchBltROP</b> function performs a stretching bit-block transfer using a <a href="/windows-hardware/drivers/">ROP</a>.

## -parameters

### -param psoDest [in, out]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to draw.

### -param psoSrc [in, out]

Pointer to a SURFOBJ structure that describes the source surface for the bit-block transfer.

### -param psoMask [in, optional]

Pointer to a SURFOBJ structure that defines a mask for the source. The mask is defined by a logic map, which is a bitmap with one bit per pixel. Typically, a mask limits the area to be modified in the destination surface. This mask is always the same size as the source surface.

### -param pco [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that limits the area to be modified in the destination. The CLIPOBJ_<i>Xxx</i> service routines are provided to enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles.

Whenever possible, GDI simplifies the clipping involved. However, unlike <a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>, <b>DrvStretchBltROP</b> can be called with a single clipping rectangle. This prevents rounding errors in clipping the output.

### -param pxlo [in, optional]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that specifies how color indices are to be translated between the source and target surfaces. If <i>pxlo</i> is <b>NULL</b>, no translation is needed.

This XLATEOBJ structure can also be queried to find the RGB color for any source index. A high quality stretching bit-block transfer will need to interpolate colors in some cases.

### -param pca [in, optional]

Pointer to a COLORADJUSTMENT structure that defines the color adjustment values to be applied to the source bitmap before stretching the bits. For more information see the Microsoft Windows SDK documentation.

### -param pptlHTOrg [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that defines the origin of the halftone brush on the destination surface. When using halftone brushes, the driver should align the upper-left pixel of the brush with this point and repeat the brush according to its dimensions. The driver should ignore this parameter if the <i>rop4</i> parameter does not require a pattern.

### -param prclDest [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that defines the rectangular area to be modified. This rectangle is specified in the coordinate system of the destination surface and is defined by two points: upper left and lower right. The two points that define the rectangle are not always well ordered, meaning the coordinates of the second point are not necessarily larger than those of the first point. The driver should interchange the two <i>x</i> values and/or the two <i>y</i> values if the destination rectangle is not well ordered.

The rectangle is lower-right exclusive; that is, it lower and right edges are not a part of the copy.

<b>DrvStretchBltROP</b> is never called with an empty destination rectangle.

### -param prclSrc [in]

Pointer to a RECTL structure that defines the area to be copied. This rectangle is specified in the coordinate system of the source surface and is defined by two points: upper left and lower right. The two points that define the rectangle are always well ordered.

The rectangle is lower-right exclusive; that is, its lower and right edges are not a part of the copy.

The driver should map this rectangle to the rectangle defined by <i>prclDest</i>.

### -param pptlMask [in, optional]

Pointer to a POINTL structure that defines a pixel in the mask to which <i>prclMask</i> points. This pixel corresponds with the upper-left pixel in the source rectangle to which <i>prclSrc</i> points. The driver should ignore this parameter if no mask is specified.

### -param iMode [in]

Specifies how source pixels are combined to get output pixels. The HALFTONE mode is slower than the other modes, but produces higher quality images. This parameter can be one of the following values:

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
On a shrinking bit-block transfer, pixels should be combined with a Boolean AND operation. On a stretching bit-block transfer, pixels should be replicated.

</td>
</tr>
<tr>
<td>
COLORONCOLOR

</td>
<td>
On a shrinking bit-block transfer, enough pixels should be ignored so pixels need not be combined. On a stretching bit-block transfer, pixels should be replicated.

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
On a shrinking bit-block transfer, pixels should be combined with a Boolean OR operation. On a stretching bit-block transfer, pixels should be replicated.

</td>
</tr>
</table>

### -param pbo [in]

Pointer to the BRUSHOBJ structure to be used to define the pattern for the bit-block transfer. GDI's <a href="/windows/desktop/api/winddi/nf-winddi-brushobj_pvgetrbrush">BRUSHOBJ_pvGetRbrush</a> service routine retrieves the device's realization of the brush. The driver can ignore this parameter if the <i>rop4</i> parameter does not require a pattern.

### -param rop4 [in]

Represents a raster operation that defines how the mask, pattern, source, and destination pixels are combined to write an output pixel to the destination surface.

This is a quaternary raster operation, which is a natural extension of the usual ternary Rop3 operation. A Rop4 has 16 relevant bits, which are similar to the 8 defining bits of a Rop3. (The other redundant bits of the Rop3 are ignored.) The simplest way to implement a Rop4 is to consider its 2 bytes separately. The lower byte specifies a Rop3 that should be computed wherever the mask to which <i>psoMask</i> points is 1. The high byte specifies a Rop3 that can be computed and applied wherever the mask is zero.

## -returns

<b>DrvStretchBltROP</b> should return <b>TRUE</b> upon success. Otherwise, it should report an error code and return <b>FALSE</b>.

## -remarks

The mapping is defined by <i>prclSrc</i> and <i>prclDest</i>. The points specified in <i>prclDest</i> and <i>prclSrc</i> lie on integer coordinates, which correspond to pixel centers. A rectangle defined by two such points is considered to be a geometric rectangle with two vertices whose coordinates are the given points, but with 0.5 subtracted from each coordinate. (POINTL structures are shorthand notation for specifying these fractional coordinate vertices.) 

The driver can optionally implement <b>DrvStretchBltROP</b>. If the driver does hook this call, it can call <a href="/windows/desktop/api/winddi/nf-winddi-engstretchbltrop">EngStretchBltROP</a> to perform those stretching blit operations that it does not support.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvalphablend">DrvAlphaBlend</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvplgblt">DrvPlgBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstretchblt">DrvStretchBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvtransparentblt">DrvTransparentBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engalphablend">EngAlphaBlend</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engbitblt">EngBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engplgblt">EngPlgBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engstretchblt">EngStretchBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engstretchbltrop">EngStretchBltROP</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engtransparentblt">EngTransparentBlt</a>