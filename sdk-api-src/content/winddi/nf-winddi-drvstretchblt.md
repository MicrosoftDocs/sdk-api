---
UID: NF:winddi.DrvStretchBlt
title: DrvStretchBlt function (winddi.h)
description: The DrvStretchBlt function provides stretching bit-block transfer capabilities between any combination of device-managed and GDI-managed surfaces.
helpviewer_keywords: ["DrvStretchBlt","DrvStretchBlt function [Display Devices]","ddifncs_7df09cb9-b2df-4ec9-a207-0f1cc8f74536.xml","display.drvstretchblt","winddi/DrvStretchBlt"]
old-location: display\drvstretchblt.htm
tech.root: display
ms.assetid: 3520533d-4e42-4abc-bc10-557c674caa33
ms.date: 12/05/2018
ms.keywords: DrvStretchBlt, DrvStretchBlt function [Display Devices], ddifncs_7df09cb9-b2df-4ec9-a207-0f1cc8f74536.xml, display.drvstretchblt, winddi/DrvStretchBlt
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
 - DrvStretchBlt
 - winddi/DrvStretchBlt
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
 - DrvStretchBlt
---

# DrvStretchBlt function


## -description

The <b>DrvStretchBlt</b> function provides stretching bit-block transfer capabilities between any combination of device-managed and GDI-managed surfaces.

## -parameters

### -param psoDest [in, out]

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that identifies the surface on which to draw.

### -param psoSrc [in, out]

Pointer to the SURFOBJ structure that defines the source for the bit-block transfer operation.

### -param psoMask [in, optional]

Optional pointer to a SURFOBJ structure that defines a surface that provides a mask for the source. The mask is defined by a logic map, which is a bitmap with 1 bit per pixel.

The mask limits the area of the source that is copied. If this parameter is specified, it has an implicit <i>rop4</i> of 0xCCAA, meaning the source should be copied wherever the mask is one, but the destination should be left alone wherever the mask is zero.

When this parameter is <b>NULL</b>, there is an implicit <i>rop4</i> of 0xCCCC, which means that the source should be copied everywhere in the source rectangle.

The mask will always be large enough to contain the relevant source; tiling is unnecessary.

### -param pco [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that limits the area to be modified in the destination. GDI services are provided to enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles.

Whenever possible, GDI simplifies the clipping involved. However, unlike <a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>, <b>DrvStretchBlt</b> can be called with a single clipping rectangle. This prevents rounding errors in clipping the output.

### -param pxlo [in, optional]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that specifies how color indices are to be translated between the source and target surfaces. If <i>pxlo</i> is <b>NULL</b>, no translation is needed.

The XLATEOBJ structure can also be queried to find the RGB color for any source index. A high quality stretching bit-block transfer will need to interpolate colors in some cases.

### -param pca [in, optional]

Pointer to a COLORADJUSTMENT structure that defines the color adjustment values to be applied to the source bitmap before stretching the bits. (See the Microsoft Windows SDK documentation.)

### -param pptlHTOrg [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that specifies the origin of the halftone brush. Device drivers that use halftone brushes should align the upper left pixel of the brush's pattern with this point on the device surface.

### -param prclDest [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that defines the area to be modified in the coordinate system of the destination surface. This rectangle is defined by two points that are not necessarily well ordered, meaning the coordinates of the second point are not necessarily larger than those of the first point. The rectangle they describe does not include the lower and right edges. This function is never called with an empty destination rectangle.

<b>DrvStretchBlt</b> should interchange the two <i>x</i> values and/or the two <i>y</i> values when the destination rectangle is not well ordered.

### -param prclSrc [in]

Pointer to a RECTL structure that defines the area that will be copied in the coordinate system of the source surface. The rectangle is defined by two points, and will map onto the rectangle defined by <i>prclDest</i>. The points of the source rectangle are well ordered. This function is never given an empty source rectangle.

The mapping is defined by <i>prclSrc</i> and <i>prclDest</i>. The points specified in <i>prclDest</i> and <i>prclSrc</i> lie on integer coordinates, which correspond to pixel centers. A rectangle defined by two such points is considered to be a geometric rectangle with two vertices whose coordinates are the given points, but with 0.5 subtracted from each coordinate. (POINTL structures should be considered a shorthand notation for specifying these fractional coordinate vertices.) 

The edges of any rectangle never intersect a pixel, but go around a set of pixels. The pixels inside the rectangle are those expected for a "lower-right exclusive" rectangle. <b>DrvStretchBlt</b> will map the geometric source rectangle exactly onto the geometric destination rectangle.

### -param pptlMask [in, optional]

Pointer to a POINTL structure that specifies which pixel in the given mask corresponds to the upper left pixel in the source rectangle. Ignore this parameter if no mask is specified.

### -param iMode [in]

Specifies how source pixels are combined to get output pixels. The HALFTONE mode is slower than the other modes, but produces higher quality images.

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
On a shrinking bit-block transfer, enough pixels should be ignored so that pixels don't need to be combined. On a stretching bit-block transfer, pixels should be replicated.

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

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.

## -remarks

<b>DrvStretchBlt</b> enables the device driver to write to GDI bitmaps, especially when the driver can perform halftoning. This function allows the same halftoning algorithm to be applied to GDI bitmaps and device surfaces.

This function can be provided to handle only certain forms of stretching, such as by integer multiples. If the driver has hooked the call and is asked to perform an operation it does not support, the driver should forward the data to <a href="/windows/desktop/api/winddi/nf-winddi-engstretchblt">EngStretchBlt</a> for GDI to handle.

If the driver wants GDI to handle halftoning, and wants to ensure the proper <i>iMode</i> value, the driver can hook <b>DrvStretchBlt</b>, set <i>iMode</i> to HALFTONE, and call back to GDI with <a href="/windows/desktop/api/winddi/nf-winddi-engstretchblt">EngStretchBlt</a> with the set <i>iMode</i> value.

<b>DrvStretchBlt</b> is optional for display drivers.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engstretchblt">EngStretchBlt</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a>