---
UID: NF:winddi.EngStretchBlt
title: EngStretchBlt function (winddi.h)
description: The EngStretchBlt function causes GDI to do a stretching bit-block transfer.
helpviewer_keywords: ["EngStretchBlt","EngStretchBlt function [Display Devices]","display.engstretchblt","gdifncs_936bc1b7-36b7-4f4f-8de4-9a4b845ac0c1.xml","winddi/EngStretchBlt"]
old-location: display\engstretchblt.htm
tech.root: display
ms.assetid: e8f3084c-6216-497b-923a-adef3bfe8bf7
ms.date: 12/05/2018
ms.keywords: EngStretchBlt, EngStretchBlt function [Display Devices], display.engstretchblt, gdifncs_936bc1b7-36b7-4f4f-8de4-9a4b845ac0c1.xml, winddi/EngStretchBlt
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
 - EngStretchBlt
 - winddi/EngStretchBlt
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
 - EngStretchBlt
---

# EngStretchBlt function


## -description

The <b>EngStretchBlt</b> function causes GDI to do a stretching bit-block transfer.

## -parameters

### -param psoDest

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to draw.

### -param psoSrc

Pointer to a SURFOBJ structure that describes the source surface for the bit-block transfer.

### -param psoMask

Pointer to a SURFOBJ structure that defines a mask for the source. The mask is defined by a logic map, which is a bitmap with one bit per pixel.

The mask limits the area of the source that is copied. If this parameter is specified, it has an implicit <i>rop4</i> of 0xCCAA, meaning the source should be copied wherever the mask is 1, but the destination should be left alone wherever the mask is 0.

If this parameter is <b>NULL</b>, the <i>rop4</i> is implicitly 0xCCCC, which means the source should be copied everywhere in the source rectangle.

### -param pco

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that limits the area to be modified in the destination. GDI services are provided to enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles.

Whenever possible, GDI simplifies the clipping involved. However, unlike <a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>, <b>EngStretchBlt</b> can be called with a single clipping rectangle. This prevents rounding errors in clipping the output.

### -param pxlo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that specifies how color indices are to be translated between the source and target surfaces.

This XLATEOBJ structure can also be queried to find the RGB color for any source index. A high quality stretching bit-block transfer will need to interpolate colors in some cases.

### -param pca [in]

Pointer to a COLORADJUSTMENT structure that defines the color adjustment values to be applied to the source bitmap before stretching the bits. For more information, see the Microsoft Windows SDK documentation.

### -param pptlHTOrg [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that defines the origin of the halftone brush. Drivers that use halftone brushes should align the upper left pixel of the brush's pattern with this point on the device surface.

### -param prclDest [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that defines the area to be modified in the coordinate system of the destination surface. This rectangle is defined by two points that are not well ordered, meaning the coordinates of the second point are not necessarily larger than those of the first point. The rectangle described does not include the lower and right edges. This function is never called with an empty destination rectangle.

If the destination rectangle is not well ordered, <b>EngStretchBlt</b> makes it well ordered.

### -param prclSrc [in]

Pointer to a RECTL structure that defines the area to be copied, in the coordinate system of the source surface. The rectangle will map to the rectangle defined by <i>prclDest</i>. This function is never given an empty source rectangle, and the points of the source rectangle are always well-ordered.

The mapping is defined by <i>prclSrc</i> and <i>prclDest</i>. The points specified in <i>prclDest</i> and <i>prclSrc</i> lie on integer coordinates, which correspond to pixel centers. A rectangle defined by two such points is considered to be a geometric rectangle with two vertices whose coordinates are the given points, but with 0.5 subtracted from each coordinate. (POINTL structures are shorthand notation for specifying these fractional coordinate vertices.) 

The edges of any rectangle never intersect a pixel, but go around a set of pixels. The pixels that are inside the rectangle are those expected for a lower-right exclusive rectangle. <b>EngStretchBlt</b> maps the geometric source rectangle exactly onto the geometric destination rectangle.

### -param pptlMask

Pointer to a POINTL structure that defines the pixel in the given mask that corresponds to the upper left pixel in the source rectangle. This parameter is ignored if no mask is specified.

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

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b> and an error code is reported.

## -remarks

This function allows the same halftoning algorithm to be applied to GDI bitmaps and device surfaces.

The driver should call <b>EngStretchBlt</b> if it has hooked <a href="/windows/desktop/api/winddi/nf-winddi-drvstretchblt">DrvStretchBlt</a> and is called to do something the driver does not support.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstretchblt">DrvStretchBlt</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a>