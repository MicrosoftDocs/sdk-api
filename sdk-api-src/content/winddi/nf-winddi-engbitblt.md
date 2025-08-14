---
UID: NF:winddi.EngBitBlt
title: EngBitBlt function (winddi.h)
description: The EngBitBlt function provides general bit-block transfer capabilities either between device-managed surfaces, or between a device-managed surface and a GDI-managed standard format bitmap.
helpviewer_keywords: ["EngBitBlt","EngBitBlt function [Display Devices]","display.engbitblt","gdifncs_ec19b94a-e653-4ecb-9c5a-2ddc8d1745c6.xml","winddi/EngBitBlt"]
old-location: display\engbitblt.htm
tech.root: display
ms.assetid: e99dbe54-485b-4a56-9956-2965f04020db
ms.date: 12/05/2018
ms.keywords: EngBitBlt, EngBitBlt function [Display Devices], display.engbitblt, gdifncs_ec19b94a-e653-4ecb-9c5a-2ddc8d1745c6.xml, winddi/EngBitBlt
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
 - EngBitBlt
 - winddi/EngBitBlt
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
 - Ext-MS-Win-moderncore-Win32k-base-ntgdi-l1-1-0.dll
 - win32kfull.sys
 - win32kmin.sys
api_name:
 - EngBitBlt
---

# EngBitBlt function


## -description

The <b>EngBitBlt</b> function provides general bit-block transfer capabilities either between <a href="/windows-hardware/drivers/">device-managed surfaces</a>, or between a device-managed surface and a GDI-managed standard format bitmap.

## -parameters

### -param psoTrg

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that identifies the surface on which to draw.

### -param psoSrc

If the <i>rop4</i> requires it, pointer to a SURFOBJ structure that defines the source for the bit-block transfer operation.

### -param psoMask

Pointer to a SURFOBJ structure that defines a surface to be used as a mask. The mask is defined as a bitmap with 1 bit per pixel. Typically, a mask limits the area that is to be modified in the destination surface. Masking is selected by a <i>rop4</i> with the value 0xAACC. The destination surface is unaffected when the mask is zero.

The mask is large enough to cover the destination rectangle.

If the value of this parameter is <b>NULL</b> and a mask is required by the <i>rop4</i>, then the implicit mask in the brush is used. If a mask is required, then <i>psoMask</i> overrides the implicit mask in the brush.

### -param pco

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure. The <b>CLIPOBJ_</b><i>Xxx</i> service routines are provided to enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles. This enumeration limits the area of the destination that will be modified. Whenever possible, GDI simplifies the clipping involved; for example, this function is never called with a single clipping rectangle. GDI clips the destination rectangle before calling this function, making additional clipping unnecessary.

### -param pxlo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that tells how color indices should be translated between the source and target surfaces.

### -param prclTrg

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure in the coordinate system of the destination surface that defines the area to be modified. The rectangle is defined by two points; upper left and lower right. The lower and right edges of this rectangle are not part of the bit-block transfer, meaning the rectangle is lower right exclusive.

<b>EngBitBlt</b> is never called with an empty destination rectangle. The two points that define the rectangle are always well ordered.

### -param pptlSrc

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that defines the upper left corner of the source rectangle, if a source exists. If there is no source, the driver should ignore this parameter.

### -param pptlMask

Pointer to a POINTL structure that defines which pixel in the mask corresponds to the upper left corner of the destination rectangle. If no mask is specified in <i>psoMask</i> the driver should ignore this parameter.

### -param pbo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure to be used to define the pattern for the bit-block transfer. GDI's <a href="/windows/desktop/api/winddi/nf-winddi-brushobj_pvgetrbrush">BRUSHOBJ_pvGetRbrush</a> service routine retrieves the device's realization of the brush. The driver can ignore this parameter if the <i>rop4</i> parameter does not require a pattern.

### -param pptlBrush

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that defines the origin of the brush in the destination surface. The upper left pixel of the brush is aligned at this point and the brush repeats according to its dimensions. Ignore this parameter if the <i>rop4</i> parameter does not require a pattern.

### -param rop4 [in]

Represents a raster operation that defines how the mask, pattern, source, and destination pixels are combined to write an output pixel to the destination surface.

This is a quaternary raster operation, which is a natural extension of the usual ternary Rop3 operation. A Rop4 has 16 relevant bits, which are similar to the 8 defining bits of a Rop3. (The other, redundant bits of the Rop3 are ignored.) The simplest way to implement a Rop4 is to consider its 2 bytes separately. The lower byte specifies a Rop3 that should be computed wherever the mask is 1. The high byte specifies a Rop3 that can be computed and applied wherever the mask is 0.

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.

## -remarks

If a device's surface is organized as a standard-format bitmap, the driver can request that GDI perform the bit-block transfer by calling <b>EngBitBlt</b>. A driver might do this if it has special hardware to handle simple transfers quickly, but doesn't want to handle calls with complicated transfers.

See the Microsoft Windows SDK documentation for more information about raster operations.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-brushobj_pvgetrbrush">BRUSHOBJ_pvGetRbrush</a>



<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a>